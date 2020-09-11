# Azure Resource Manager, Policies and Locks

## Azure Resource Manager 

* Deployment and management service for Azure. It's a management layer that enables you to create, update and delete resources.

* **Resource** - service aviable in Azure Cloud (VMs, Databases, Storage Account)
* **Resource Groups** - container that encompasses multiple related resources
* **Resource Provider** - Family of related Azure resources 
* **Resource Manager Template** - JSON file that defines resources to be deployed.
* **Benefits**
    - Manage your infrastructure through templates -> JSON file includes the properties for the infrastructure to deploy.
    - Deploy resources in the correct oder -> dependencies between Azure resources
    - Centrally deploy, manage and monitor all your resources.
    - Apply tags to resources to logically organize them.
    - Clear billing and costs at the organization level -> tags
* **Management Levels**
    - Management Groups
    - Subscriptions
    - Resource Groups
    - Resources
* **Templates**
    - It is possible to make mistakes while manually deploying resources in Azure.
    - It is time consuming to deploy resources in Azure
    - Deployments can be automated through infrastructure as code. In the actual code you can define the infrastructure that will be deployed and how it will deployed (order of deployment, resources properties
* **Infrastructure as Code (IaC)**
    - Automate infrastructure deployment throug proprietary 
    - Azure -> Azure Resource Manager
    - AWS -> AWS CloudFormation
    - GCP -> Google Cloud Deployment Manager
    - Terraform, Chef, Ansible, Puppet
* **Declarative Syntax** - Deploy an entire infrastructure
* **Depployment Orchestration** - Orchesstrate the deployment of interdependent resources, so that they are deployed in the correct order.
* Template is first validated then deployed
* Create any resource in Azure and also supports integration with CI/CD tools.


## Resource Groups

* Logical Containers for resources deployed on Azure
* All deployed resources (Azure services) are part of a single resource group and can be moved between RGs later on.
* BTW, resources in RG can be deployed in different Azure regions, no restriction here.
* In simple terms, we use RGs to better manage and organize our resources in Azure
* **Resource Groups Location**
    - Resources in a RG can be part of any region but RGs are tied to a specific region.
* **Resource Groups Naming Convention**
    - <Resource><Subscription Type><Region>
        * VNET-Shared01-WestUS
* **Organizing Principles**
    - By environment
    - By resource type
    - By department
    - By admin type
    - By lifecycle 
    - Billing reports purposes
* **Takeway**
    - Invest time before starting your work in Azure, in order to define a clear, straightforward structure.
    - Lots of options exist, leverage Azure flexibility in your advantage.

## Azure Tags

* Tags are name/value pairs of text data that apply to resources and resource groups.
* You can attach/bind up to 50 tags to a resource 
* **Use cases**
    - Cost Center
    - Department
    - Environment
    - Automation start or shutdown
* Define a procedure stating that all resources must have tags attached
* You can enforce tagging rules and naming conventiosn throughout your organization with Azure Policies.

## Azure Policy 

* A service you can use to create, assign and manage policies
* Establishes conventions or rules that resources must comply with
* Example -> Create resources only in "westeurope"
* **Policy Definition** -> conditions and effect
* **Policy assignment** 
    - assign the policy definition to a specific scope 
    - inherited by all child resources
* **Built-in Azure Policies**
    - Available by default, covering common scenarios
    - **Allowed Locations** -> New resources to be deployed in specific locations
    - **Allowed Virtual Machines SKUs** -> Only specific VM SKUs to be used
    - **Enforce tag and its value** -> Enforces a required tag and its value to a resource.
* **Initiative Definitions** - apply multiple policies at once.


## Azure Locks

* Prevent users in your organization from accidentally deleting or modifying critical resources.
* **Options Available**
    - **Delete** -> Read and Modify a resource, can't Delete
    - **Read-only** -> Read a resource, can't Modify or Delete
* Similar to Azure Policies, when you apply Locks at a parent scope, all resources within that scope will inherit the lock.