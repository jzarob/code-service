# code-service

## Environment Variables

|Environment Variable |Description                                               |Example|
|---------------------|----------------------------------------------------------|-------|
|CUSTOMCONNSTR_code-db|The URI Connection String to connect to the Mongo Database|mongodb://user:password@host:port|
|CODE_WEB_URI         |The base address for the Client Application (ng)          |http://code-web-ui.azurewebsites.net|
|CODE_SERVICE_URI     |The URI of the running service instance                   |http://code-service.azurewebsites.net/api/v1|

## Deployment Instructions

```sh
mvn package
python3 azure-deploy.py -d target/ --host ${AZURE_HOST} -u code-service\\${DEPLOY_USER}
```