## Introduction

- Vert.x is reactive, scalable and resilient in nature.
- Vert.x solves the waiting time problem of a multi-threaded application by introducing event bus and processing the requests as fast as possible.

## Vert.x Core
- MainVerticle is the entry point of Vert.x project.
- By default an empty application, vertx starts at port 8888.
- Each verticle must be delployed by vertx object. vertx object can also undeploy a verticle.
- Each parent verticle has control to deploy and undeploy child verticle.
- Each verticle can be deployed multiple times to achieve scalability and concurrency.
- All verticles uses same vert.x instance.
- Same verticle can be deployed multiple times by passing class name as first param to vertx.deployVerticle()
-  

## Errors and Fixes
- Configuring java version for the project is present under **Project Structure (cmd+;)**
