## The package includes three services:

**discovery-service** - service which is based on 
the eureka the main purpose is to register an application.<br/> 
**business-service** - The service provides the only one endpoint that 
returns the application version.<br/>
**gateway-service** - The gateway to business_api with the only one endpoint (_/business_)<br/>
## Building

### Production
In order to build the services the command should be used:<br/>
_mvn clean install && docker-compose build_ <br/>
The default environment will be used which is for production and stored in _.env_ file.

### Test
For test server this command should be used
_mvn clean install && docker-compose --env-file .env-dev build_ <br/>
The command builds the containers using testing environment which is stored in _.env-dev_ file.

## Starting the app
To start the app use this command 
_docker-compose up -d_
The command can be launched with additional argument with environment path:
_docker-compose --file-env .env-dev up -d_ <br/>
## Environment
All the necessary environment stored in the "__./.env__" file.

## Using the app

To use the app send GET request on gateway-service service. <br/>
For example if the service deployed on localhost the curl request will be:<br/>
_GET /business HTTP/1.1
Host: localhost:8082_