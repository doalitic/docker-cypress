# Cypress Docker images

These images provide all of the required dependencies for running Cypress in Docker. They're based
on the [official Cypress images](https://github.com/cypress-io/cypress-docker-images), but adapted
to the development toolchain employed by the team in charge of the web front-end of
[Moss](https://moss.sh).

E.g. these images may differ with respect to the official ones in the versions of **Node.js**,
**Chrome** or **Firefox** that they contain.


## Images

All images are available on Docker Hub.

| Image | Node.js | Browsers | Status |
| ----- | ------- | -------- | ------ |
| [doalitic/cypress-base:8](base/8) | 8.11 | - | [![Docker Build Status](https://img.shields.io/docker/build/doalitic/cypress-base.svg)](https://hub.docker.com/r/doalitic/cypress-base/) |
| [doalitic/cypress-chrome:stable](chrome/stable) | 8.11 | Chrome 65 | [![Docker Build Status](https://img.shields.io/docker/build/doalitic/cypress-chrome.svg)](https://hub.docker.com/r/doalitic/cypress-chrome/) |
| [doalitic/cypress-firefox:59](firefox/59) | 8.11 | Firefox 59 | [![Docker Build Status](https://img.shields.io/docker/build/doalitic/cypress-firefox.svg)](https://hub.docker.com/r/doalitic/cypress-firefox/) |


## Usage

Example **Dockerfile**s to install and run Cypress.

- Chrome:

  ```docker
  FROM doalitic/cypress-chrome:stable
  
  RUN npm install cypress
  RUN $(npm bin)/cypress run --browser chrome
  ```

- Firefox:

  ```docker
  FROM doalitic/cypress-firefox:59
  
  RUN npm install cypress
  RUN firefox --version
  RUN $(npm bin)/cypress run --browser firefox
  ```

- Sure you get the idea :D For more images, please see the table above.


## Contributing

Most likely you'll be willing to contribute to the
[official Cypress images](https://github.com/cypress-io/cypress-docker-images). If for whatever
reason you find these images more appropriate for your setup and want to contribute to them, please
feel free to create a PR and we'll be happy to review it :D
