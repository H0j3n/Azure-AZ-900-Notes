# Azure Compute Options


## Azure Compute

* Azure compute is an on-demand computing service that facilitates running your Apps in the cloud.
* Resources in Azure are available on-demand in minutes or even seconds (depends on the compute option)
* VMs, Containers, Azure App Service & Serverless

**Virtual Machine (VMs)**

* Running in the lcoud. Virtualiez the hardware layer, the physical infrastructure, and compromise - vCPU, vMemory, vStorage and vNIC.
* A guest OS can be installed (on the VM), separate and totally independent from the host OS (server)/
* VMs act as physical computers.

**Containers**

* Just like VMs, containers can be used in order to run your Apps in the cloud.
* Differences which containers don't own an OS, containers start in milliseconds (ms) and containers use far less storage.
* Like docker container.

<p align="center">
<img src="https://github.com/H0j3n/Azure-AZ-900-Notes/blob/master/img/aks.png" alt="My Images"></p>

* You can easily run containers on Azure without managing servers -> **Azure Container Instances (ACI)**
* ACI (Azure PaaS offering) allows uploading your containers to Azure and running them immediately.
* No virtual machines to manage, no additional configration needed.

<p align="center">
<img src="https://github.com/H0j3n/Azure-AZ-900-Notes/blob/master/img/aci.png" alt="My Images"></p>


* Azure Kubernetes Service (AKS) makes deploying and managing containerized applications easy.
* AKS is a complete orchestration service for containers with distributed architectures with multiple containers.
* Orchestration - use AKS in order to automate, manage, and interact with a large number of containers.

**Azure App Service**

* Platform-as-a-service (PaaS)
* With Azure App Service you can build web apps in the programming language of your choice without managing infrastructure.
* Pricing based on App Service Plan
* With App Service, apps run in an App Service plan. When create an App Service plan, a set of compute resources is created for that plan in that region.
* Each App Service plan defines -> Region, Number of VM instances, size of VMs and pricing tier
* The pricing tier of an App Service plan determines what App Service features you get and how much you pay for the plan.
* Three pricing tiers:
    - **Shared Computer: Free and Shared** - The app is run on the same VM as other apps and scaling is not an option.
    - **Dedicated Compute: Basic, Standard, Premium** - Apps are run on dedicated VMs and apps in the same App Service plan share the same compute resource.
    - **Isolated: Dedicated VMs run in dedicated vNETs**
* Types of Web Apps:
    - **Web Apps** - Build & Deploy web apps faster at scale.
    - **API Apps** - Easily build and consume APIs//
    - **Web App for Containers** - Deploy and run containerized web apps.
    
**Azure Functions : Serverless**

* Serverless computing enables developers to build applications faster by eliminating the need for them to manage infrastructure.
* With serverless applications Azure automatically provisions, scales and manages the infrastructure required to run the code.
* Build app -> execute (create index.html and run it in a cloud ready environment)
* Main pillars:
    - **Abstration of Servers**
    - **Even-driven**
    - **Pay by The Run Time**
## Comparing Virtual Machine vs Containers

<p align="center">
<img src="https://github.com/H0j3n/Azure-AZ-900-Notes/blob/master/img/vmcontainer.png" alt="My Images"></p>

# References

1. https://azure.microsoft.com/en-us/overview/what-is-cloud-computing/

2. https://azure.microsoft.com/en-in/overview/what-is-a-container/#:~:text=Containers%20explained&text=A%20standard%20package%20of%20software,deploy%20applications%20seamlessly%20across%20environments.

3. https://azure.microsoft.com/en-us/services/container-instances/

4. https://azure.microsoft.com/en-us/services/app-service/