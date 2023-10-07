### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

--------------------
#### Analysis

**Costs**:
In terns of cost, an App service would be mmore flexible since more than one app can be made to share
the App Service plan. A Virtual machine has the advantage of being able to be deallocated when not in use
in order to cut costs

**Availability**:
In terms of availability Virtual machines generally have more availability than App Services, but require extra setup and configuration to be fault tolerant and avoid downtimes during maintenance and upgrades

**Scalability**:
Both the VM and the App Service can be scalled horizontally and vertically. VMs can be scalled horizontally using a VMSS, while App Service's have native Auto scalling properties


**Workflow**:
It is fairly easier to deploy applications to App Service than it is to Virtual Machines. Although an automated CI/CD pipeline could be designed to resolve this issue.

--------------------
#### Decision

Deployment option: App Service https://duong12-uda-appservice.azurewebsites.net/login

--------------------
#### Justification

An App Service is a PaaS offering meaning that you just have to deploy your code and not worry about the underlying infrastructure. The application is designed to be cloud native removing the need for server management and optimization. It also has good pricing tiers and gives adequate room for scalability. Another caveat is the wide range of deployment options available that can easily be integrated into a production workflow

--------------------

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.*

App Service has some limited including :
 - The web app can utilize the surplus space from other plans within the same webspace, exceeding the limit of its own plan. However, it's important to note that this practice is not recommended.
 - The app service can only be migrated to different plans within the same webspace.
 - The max limit is 500 Gb for webspace for Apps hosted on multi-tenant and 1 Tb for ASE
 - We can remote to appservice