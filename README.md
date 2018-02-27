# Sample MicroProfile OpenAPI Application

This application is derived from the [MicroProfile OpenAPI TCK](https://github.com/eclipse/microprofile-open-api/tree/master/tck)

## Setup and run instructions

### Clone application
*  `git clone https://github.com/microservices-api/oas3-microprofile-app.git`

### Create a deployable WAR file

*  `cd oas3-microprofile-app`
*  `mvn package`

The packaged WAR file will be at the following location: `oas3-microprofile-app/deployment_artifacts/airlines.war`

### Deploy locally in a Docker container (using Open Liberty)
* `cd deployment_artifacts`
* `docker build -t demo .`
* `docker run -d -p 80:9080 demo`
* open a browser and navigate to `localhost/openapi` to see the OpenAPI document, and `localhost/openapi/ui` to see the OpenAPI UI.
