# Trusted Application Pipeline Software Template

This application, **rhtap-e2e**, was created from a Trusted Application Pipeline Software Template.

The software templates create a new source and gitops deployment repositories with a sample source application. 

## Repositories

The source code for your application can be found in [https://github.com/rhtap-hub/rhtap-e2e ](https://github.com/rhtap-hub/rhtap-e2e ).
 
The gitops repository, which contains the kubernetes manifests for the application can be found in 
[https://github.com/rhtap-hub/rhtap-e2e-gitops ](https://github.com/rhtap-hub/rhtap-e2e-gitops ) 

## Application namespaces 

The default application will be found in the following namespaces. Applications can be deployed into unique namespaces or multiple software templates can also bet generated into the same group namespaces.  

|  Namespace   |  Description   |  
| -------- | -------- |   
| **rhtap-e2e-development** | The default application during development. Every build will be deployed to this namespace for testing. | 
| **rhtap-e2e-stage** | The staging namespace for this application. Promotion from development to stage is manual via an update to the [gitops repository](https://github.com/rhtap-hub/rhtap-e2e-gitops ) in the components/rhtap-e2e/overlays/prod directory |  
| **rhtap-e2e-prod** | The production namespace for this application. Promotion from stage to production is manual via an update to the [gitops repository](https://github.com/rhtap-hub/rhtap-e2e-gitops ) in the components/rhtap-e2e/overlays/prod directory | 