# camunda-playground
A basic setup to play with the Camunda workflow engine.

# Setup
## Pre-Requesites
- a suitable JDK (14 +), e.g. from https://adoptopenjdk.net/releases.html?variant=openjdk14&jvmVariant=hotspot
- maven if you choose to use the pom.xml provided
- Docker
- curl or Postman
- Camunda Modeler: https://camunda.com/download/modeler/ 

## Running it
- cd into this project
- start the docker container with Camunda engine

`cd docker-engine && docker-compose -f stack.yml up`

- Run the ChargeCardWorker java class... I leave figuring this out to you, I am using vscode and maven as it makes things a lot easier
- Execute a request via postman or curl to trigger the workflow