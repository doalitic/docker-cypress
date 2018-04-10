# doalitic/cypress-firefox

Firefox images with all required dependencies for running Cypress in Docker. They're based
on the [official Cypress images](https://github.com/cypress-io/cypress-docker-images), but adapted
to the development toolchain employed by the team in charge of the web front-end of
[Moss](https://moss.sh).


## Images

All images are available on Docker Hub. They are tagged with the Firefox version they contain.

| Image | Node.js | Browsers | Status |
| ----- | ------- | -------- | ------ |
| [doalitic/cypress-firefox:59](firefox/59) | 8.11 | Firefox 59 | [![Docker Build Status](https://img.shields.io/docker/build/doalitic/cypress-firefox.svg)](https://hub.docker.com/r/doalitic/cypress-firefox/) |


## Usage

Example **Dockerfile**s install and run Cypress.

```docker
FROM doalitic/cypress-firefox:59

RUN npm install cypress
RUN firefox --version
RUN $(npm bin)/cypress run --browser firefox
```
