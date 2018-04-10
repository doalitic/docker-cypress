# doalitic/cypress-base

Base images with all required dependencies for running Cypress in Docker. They're based
on the [official Cypress images](https://github.com/cypress-io/cypress-docker-images), but adapted
to the development toolchain employed by the team in charge of the web front-end of
[Moss](https://moss.sh).


## Images

All images are available on Docker Hub. They are tagged with the Node.js version they contain.

| Image | Node.js | Browsers | Status |
| ----- | ------- | -------- | ------ |
| [doalitic/cypress-base:8](base/8) | 8.11 | - | [![Docker Build Status](https://img.shields.io/docker/build/doalitic/cypress-base.svg)](https://hub.docker.com/r/doalitic/cypress-base/) |


## Usage

Example **Dockerfile** to install and run Cypress.

```docker
FROM doalitic/cypress-base:8

RUN npm install cypress
RUN $(npm bin)/cypress run
```
