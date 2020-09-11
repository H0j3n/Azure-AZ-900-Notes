# Security in Azure

## Azure Cloud Shared Responsibility Model

* Responsibility is shared between the cloud provider and the client and the responsibility level depends on type of apps and cloud deployment model.

## Security - Layer over Layer over Layer

* The best way to implement security in the cloud or traditional infrastructures is to consider using multiple security layers.
* The first layer of defense is physical security
    - DC Security, cameras, restricted access
* Implement identity and access-based security (SSO & MFA)
    - Control access based on identities
    - Grant minimum access
    - Keep track of events
* Network Perimiter Security
    - DDoS protection & Firewall security
* Restrict or Limit network connectivity
    - Deny inbound network connectivity
    - Limit connectivity between resources
    - Security to on-prem DC
* Security for Compute
    - Patch VMs, implement endpoint protection 
    - Implement secure access to VMs
* Security for Applications
    - Integrate security in app dev lifecycle
* Data Security
    - Customer's responsibility
    - Many tools available
* Examples
    - Data Stored in DBs
    - Data Stored in disks (VMs)
    - Data Stored in Cloud Storage

## Azure Security Center

* Monitoring service that provides threat protection accross all of your services both in Azure and on-premises infrastructures.
* Capabilities
    - **Strengthen security posture** - Identifies security issues and implements best practices across your machines, data services and apps.
    - **Protect against threats** - Evaluates workloads and raises threat prevention recommendations and security alerts.
    - **Get your environment secure faster** - Security is implemented at cloud speed.
* **Tiers**
    - **Free**
        * Tier limited to assessments and recommendations
        * Azure Secure Score
    - **Standard**
        * Continuous monitoring, threat detection, etc.

## Azure Identity Services

*  **Authentication** - establishes if the user (or service) is who it says it is. Identity is challenged and checked through username and password or authentication keys, certs
* **Authorization** - once the user or service is authenticated, authorization establishes what level of access should be provided. Read-only, editor, full admin. What resources and what permissions.

## Azure Active Directory (AD)

* Microsoft's cloud-based identity service, that can also integrate with your traditional on-premises infrastructure.
* All your applications, running either in the cloud or on traditional infrastructures, can share the same credentials.
* As a result of this, with Azure AD you centralize access control to all your apps and data, with a single pane of glass over identity management.
* **Capabilities**
    - **Authentication**
        * Identity verification for access to apps and resources
    - **Single-Sign-On (SSO)**
        * Users can use a single identity (username & password) for authentication on all company apps.
    - **User management** 
        * Customize and control how your users sign up, sign in. Manage guest users and external partners when using your apps.
    - **Conditional Access to your apps**
    - **Device Management**
        * Manage how your cloud or on-premises devices access your corporate data
    - **Privileged Identity Management (PIM)**
        * Manage, control and monitor access within your organization.
* **Azure Privileged Identity Management (PIM)**
    - Service that enables you to manage,control and monitor access to resources in your organizations
    - PIM provides time-based and approval-based role activation on resources that you care about.
* Examples
    - Assign time-bound access to resources
    - Role activation upon approval
    - Enforce MFA to activate any roles
    - Get notifications when privileged roles are activated

## Multi Factor Authentication (MFA)

* Process where a user is prompted during sign-in process for an additional form of identification
    - SMS Code
    - OTP or code
    - Fingerprint scan
* Something you know -> password
* Something you have -> App on phone
* Something that you are -> biometrics
* Increases security of your identities by requesting an additional authentication factor

## Azure RBAC

* Authorization system built on Azure Resource Manager that you can use to provide granular access to Azure resources
* RBAC helps you manage **WHO** has access to Azure resources, **WHAT** they can do with those resources and **WHAT** areas they have access to.
* Grant minimum permissions (least privilege) to users or services in order to perform their job
* **Common Use Cases**
    - Allow user to manage VMs in a subscription
    - Allow an application to access all resources in RG
    - Allow user to maanage all resources in a RG, such as virtual machines, websites and subnets
    - Allow databases team to manage the SQL databases in a subscription.
* With RBAC, you can control access to resources using role assignments - it's how permissions are enforced.
* Three elements
    - Security principal
    - Role definition
    - Scope
* First we will define each of the components and last we will see how all fit together and talk about role assignments.
* **Security Principal**
    - Object that is requesting access to Azure resources -> user, group, service principal or managed identity
    - **User** -> Individual who has a profile in Azure AD
    - **Group** -> A set of users in Azure AD
    - **Service Principal** -> Security identity of an app or service
    - **Managed Identity** -> Identity in Azure AD, Azure managed
* **Role Definition**
    - A collection of permissions (operations permitted read, write and delete)
    - Includes custome roles & built-in roles
        * **Owner** -> Full admin permissions
        * **Contributor** -> Create and manage any Azure resources, but can't grant access to others
        * **Reader** -> Can view existing Azure resources
    - Other built-in roles are available, targeting specific Azure resources
* **Scope**
    - The set of resources that the access applies to
    - When you assign a role, you can further limit the actions allowed by defining a scope -> VM Contributor for a specific Resource Group
    - You can specify scope at multiple levels. Structured in a parent-child relationship
    - When you grant access at a parent scope, permissions are inherited to the child scopes.
* **Role Assignment**
    - Process of attaching a role definition to a security principal, at a particular scope for the purpose of grantin access

## Azure Firewall

* Managed , cloud-based network security service that protects your Azure Virtual Network resources.
* You can use an Azure Firewall to grant access to resources in a VNET, based on the originating/source IP address
* Only clients from these granted IP addresses will be allowed to the internal resource
* Access is permitted/denied through firewall rules, that you create and specify ranges of IP addresses.
* Supports inbound and outbound filtering


## Denial of Service (DoS) & Distributed Denial of Service (DDoS)

* **Denial of Service (DoS)** - type of attack that aims to overwhelm a network resource by sending huge number of requests, so that the resource becomes slow/unresponsive
* **Distributed Denial of Service (DDoS)** - occurs when multiple systems flood the bandwidth or resources of a targeted system, usually one or more web servers.
* Azure DDos Protection provides defense against DDoS attacks.
* **Tiers**
    - **Basic**
        * Enabled by default
        * Always-on traffic monitoring and real-time mitigation of common network-level attacks
        * Free, implies no cost
    - **Standard**
        * Advanced mitigation capabilities over Basic tier
        * Can mitigate volumetric attacks, protocol attacks and application layer attacks.
        * Price is based on usage, on a monthly basis.
* **Attack Types**
    - **Volumetric Attacks**
        * The victim is flooded (at the network layer -IP) with huge amount of traffic that seems to be legit
    - **Protocol Attacks**
        * Attack targets layer 3 and layer 4 protocol attack
        * Common example -> SYN flood attacks (TCP,layer 4)
    - **Application Layer Attacks**
        * Target web applications
        * Common examples -> SQL Injection, Cross-site scripting

## Encryption

* Process of encoding a message or information in such a way that only authorized parties can access it.
* To use or read the encrypted data, it must be decrypted which requires the use of a secret key.
* Two types of encryption available -> symmeteric and asymmeteric
* **Symmeteric Encryption**
    - Same encryption key is used to both encrypt and decrypt the data
* **Asymmeteric Encryption**
    - Public key and private key pair used.
    - Both can encrypt but you can only decrypt with the paired key
    - More secure
    - Used in HTTPS environments (PKI and certificates)
* **Encryption at rest**
    - Data at rest is the data that has been stored on a physical medium.
    - Data is not moving or travelling.
* **Encryption in transit**
    - Data in transit is the data actively moving from one location to another.
    - To on-prem DC, through the internet
    - Protects the data from outside observers and provides a mechanism to transmit data securely.
* **Azure Storage Service Encryption**
    - Protect data at rest
    - Data is automatically encrpyted before storing it to Azure Storage and decrypted before retrieval
* **Azure Transparent Data Encryption (TDE)**
    - Real-time encryption and decryption for databases Azure SQL Database and Azure Data Warehouse.
    - Enabled by default
* **Azure Key Vault** 
    - Encrypt the actual keys
    - We can ensure that the keys themselves are secure and store them in a centralized cloud service (AKV)
    - **Common Uses**
        * Secrets Managements -> stores tokens, passwords, certs
        * Key Management -> create and control encryption keys
        * Certificate Management -> provision, manage and deploy private or public certificates

## Azure Threat Protection (ATP)

* Cloud-based security solution that identifies, detects and helps you investigate advanced threats, compromised identities and malicious actions targeting your organization
* With Azure ATP, you can detect known malicious attacks, security issues and risks against your network.
* Azure ATP includes several components ->  ATP Portal, ATp sensor and ATP cloud service.
* **Azure ATP Sensors**
    - Sensors are installed directly on your domain controllers
* **Azure ATP Portal** 
    - View data received from Azure ATP Sensors
    - Monitor, manage and investigate threats in your network environment
* **ATP Cloud Service**
    - The actual cloud service that runs on Azure

## Azure Information Protection (AIP) Overview

* Cloud-based solution that helps organizations to classify and optionally, protect its documents and emails by applying labels.
* Documents and emails are applied labels, depending on what information is contained
* For example, the Admin can define rules that detect sensitive data and labels are applied automatically.
* After the content is classified you can then track and control how it is used.
* Azure Rigts Management - Encryption and authorization policies.

# References