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

`cd camunda-engine && docker-compose -f stack.yml up`

- Open the ChargeCard.bpmn model with Camunda Modeler and deploy it using the following parameters:
  - Deployment Name: "ChargeCard"
  - Tenant ID: ""
  - REST Endpoint: "http://localhost:8080/engine-rest"
- Run the ChargeCardWorker java class... I leave figuring this out to you, I am using vscode and maven as it makes things a lot easier
- Execute a request via postman or curl to trigger the workflow, e.g. using the following curl
`sh requests/process-start`
- open the browser (http://localhost:8080/camunda/app/welcome/default/#!/login) and login as demo:demo to see the manual tasks: http://localhost:8080/camunda/app/tasklist/default/
- Have fun tinkering around...
