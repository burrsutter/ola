# ola
Microservice using Spring Boot

Build and Deploy ola
--------------------

1. Open a command prompt and navigate to the root directory of this microservice.
2. Type this command to build and execute the microservice:

        mvn clean compile spring-boot:run


Access the application
----------------------

The application will be running at the following URL: <http://localhost:8080/api/ola>

## Deploy in Openshift

1. In CDK directory, export the environment variables to have access to Docker daemon

		eval "$(vagrant service-manager env docker)"

2. Type this command to build and deploy the microservice in Openshift/CDK

		mvn clean package docker:build fabric8:json fabric8:apply
