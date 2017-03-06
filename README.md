# interop-domain

domain project for interop projects


Interop Projects Overview:
![alternate text][logo]

[logo]: https://github.com/LevelOneProject/interop-domain/blob/develop/Interop_projects_overview.png "Interop Projects Overview"

This repo contains a project that contains shared properties, configurations and metrics. Currently only contains http configuration used by both SPSP and DFSP projects to enable them to run on a the same port, on a host or a docker container. Also, several spring beans are imported for reuse, among them Ledger to Ledger adpater and vice-versa URL transformer and a ledger URL mapper.

Contents:

- [Deployment](#deployment)
- [Configuration](#configuration)
- [API](#api)
- [Logging](#logging)
- [Tests](#tests)

## Deployment

Project is built using Maven and uses Circle for Continous Integration.

(How do you run this code?)

(Example for NPM-published services--

Installation:

1. Install [Node.js and npm](https://nodejs.org/en/)

2. Configure your npm instance to use the LevelOneProject repository.

    See [Docs/Artifactory/NPM Repos](https://github.com/LevelOneProject/Docs/blob/master/Artifactory/npm_repos.md) for detailed instructions.

3. Install the `(package name)` package.

        npm install (package name)

Running the server locally:

    npm start

--end example)

## Configuration

pom.xml and circle.yml can be found at interop-domain repo

(Explanation of important config parameters)


## API

The project in this repo does not offer an API, it offers a domain to shared resources by the Mule Interop projects.

## Logging

Sever path to logs is: /opt/mule/mule-dfsp1/logs

(Explain important things about what gets logged or how to interpret the logs. Use subheaders if necessary.)

## Tests

There are no tests for the domain project.
