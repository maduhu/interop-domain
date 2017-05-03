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

### Installation and Setup

#### Anypoint Studio
* [https://www.mulesoft.com/platform/studio](https://www.mulesoft.com/platform/studio)
* Clone https://github.com/LevelOneProject/interop-domain.git to local Git repository
* Import into Studio as a Maven-based Mule Project with pom.xml
* Since this is a domain project, cannot be run in isolation from Studio but in conjunction with another project that is joined to it.

#### Standalone Mule ESB
* [https://developer.mulesoft.com/download-mule-esb-runtime](https://developer.mulesoft.com/download-mule-esb-runtime)
* Add the environment variable you are testing in (dev, prod, qa, etc).  Open <Mule Installation Directory>/conf/wrapper.conf and find the GC Settings section.  Here there will be a series of wrapper.java.additional.(n) properties.  create a new one after the last one where n=x (typically 14) and assign it the next number (i.e., wrapper.java.additional.15) and assign -DMULE_ENV=dev as its value (wrapper.java.additional.15=-DMULE_ENV=dev)
* Download the zipped project from Git
* Copy zipped file (Mule Archived Project) to <Mule Installation Directory>/domains

### Run Application

#### Anypoint Studio
* Since this is a domain project, cannot be run in isolation from Studio but in conjunction with another project that is joined to it. Run As Mule Application with Maven the other base level project that is joined to the domain.

#### Standalone Mule ESB
* CD to <Mule Installation Directory>/bin -> in terminal type ./mule

## Configuration

[pom.xml](./pom.xml) and [circle.yml](./circle.yml) can be found in the repo, also linked here


## API

The project in this repo does not have an API. It contains shared resources used by the Mule Interop projects.

## Logging

Server path to logs is: <mule_home>/logs/*.log for example: /opt/mule/mule-dfsp1/logs/interop-domain.log

Currently the logs are operational and include information such as L1p-Trace-Id and other details related to the calls or transactions such as path, method used, header information and payer/payee details.

## Tests

There are no tests for the domain project.
