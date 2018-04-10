# Cypress Docker images

These images provide all of the required dependencies for running Cypress in Docker. They're based
on the [official Cypress images](https://github.com/cypress-io/cypress-docker-images), but adapted
to the development toolchain (e.g. to use the latest **node** version) employed by the team in
charge of the web front-end of [Moss](https://moss.sh).


## Images

Work in progress.


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


## Docker Hub

Work in progress.


## Contributing

Most likely you'll be willing to contribute to the
[official Cypress images](https://github.com/cypress-io/cypress-docker-images). If for whatever
reason you find these images more appropriate for your setup and want to contribute to them, please
feel free to create a PR and we'll be happy to review it :D
