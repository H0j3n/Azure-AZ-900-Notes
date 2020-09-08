# Azure Cloud Introduction


## Cloud Computing ☁️

* **Cloud computing** is the delivery of computing services which includes servers, storage, databases, networking, software, analytics and intelligence over the Internet **"cloud"** to offer faster innovation, flexible resources and economies of scale (Microsoft)

* **Cloud computing** really represents renting resources (CPU, RAM, storage) from a cloud provider (Azure) and only "pay as you go"

## Top benefits of Cloud Computing 💚

* **Cost Effective** - offers a pay as you go prricing model (consumption-based pricing model)
    * No upfront costs
    * Pay extra for resources only when needed (elasticity)
    * No infrastructure to purchase and manage
* **Scalability (Up or Down)** = Highly scalable and can acommodate any business growth
    * Can adapat to your business by scaling either vertically or horizontally
* **Elasticity** - Highly elastic and can adapt to demand changes, adding or removing resources
* **Current or Always Up to Date** - Always up to date, running on most current and recommend hardware and software versions.
    * Microsoft Azure responsible for Hardware configration
    * Microsoft Azure responsible for Software Patching
    * Microsoft Azure responsible for Software and Hardware Upgrades
    * Microsoft Azure responsible for Replacing faulty equipment
* **Global** - With Azure Cloud you can go glocal in minutes
    * Easily deploy your application in multiple regions around the world with just a few clicks
    * You can provide lower latency and better experience for your customers at minimal cost
* **Security** - Secure, enforcing strict security policies at both physical and digital layers.
    * **Physical security is Azure Cloud's responsibility** - secure Data Centers, Cameras, Locks, specialized security personnel
    * **Digital Security** - Azure provides access to resources in the cloud only to authorized users
* **Reliability** - Highly reliable, providing redundancy and fault tolerance to resources.
    * Azure Cloud Infrastructure is built in order to accomodate disasters
    * If one component fails a backup component will seamlessly take ownership to assure service availability
    * Data in your Azure storage account is replicated to ensure durability and high availability.
* **Speed**
* **Global Scale**
* **Productivity**
* **Performance**
* **Adaptability**
* **Pay As You Go**

## Types of Cloud Computing ☁️

<p align="center">
<img src="https://github.com/H0j3n/Azure-AZ-900-Notes/blob/master/img/cloud.png" alt="My Images"></p>


* **Public Cloud** - Owned and operated by Microsoft and Computing Resources **(servers, storage)** are delivered through internet
    * Pay-as-you-go pricing
    * No hardware maintenance or updates
    * Elastic, Agile, Highly Scalable and Adaptable
    * Start immediately and go global in minutes 
    * Lower costs
    * Near-unlimited scability
    * High realibility.  
* **Private Cloud** - Known as **"traditional on-premises"**, resource are deployed in your on-premises DataCenter (DC), using virtualization and resource management tools such as **VMware, Hyper-V, OpenStack**
    * Full Control over infrastructure (responsible for management and patching)
    * Meet strict security, compliance or legal requirements
    * Accomodate legacy apps
    * Full flexibility over desired configuration
    * Improve security
    * High scalability
* **Hybrid Cloud** - Combine **Public** and **Private Clouds**, allowing data and applications to be shared between them.
    * Greates flexibility - can run apps both in public and continue to run legacy or sensitive apps on-premises
    * Use on-premises servers in order to meet security, compliance and strict regulations.
    * Continue to run apps on out-of-date hardware or OS, until redesign is possible for running in the cloud

## Type of Cloud Services 🛠️

<p align="center">
<img src="https://github.com/H0j3n/Azure-AZ-900-Notes/blob/master/img/services.png" alt="My Images"></p>

* **IaaS (Infrastructure as a Service)** - Rent IT Infrastructure - servers and Virtual Machines (VMs), storage, networks, OS from Azure Cloud
    * Provides the highest level of flexibility and management control over the infrastucture
* **PaaS (Platform as a Service)** - Offers an on-demand environment for developing, testing, delivering and managing software applications.
    * Mostly used by developers
    * Quickly create a web or mobile apps without taking care of the underlying infrastructure of servers, storage, network, DBs
* **SaaS (Software as a Service)** - A method for delivering software applications over the Internet, on demand and typically on a subscription basis (monthly/yearly)
    * Do not have to think about how the service is maintained
    * Do no have to think how the underlying infrastructure is managed
    * Only need to think about how you will use the App

## CapEX and OpEx 🏢

<p align="center">
<img src="https://github.com/H0j3n/Azure-AZ-900-Notes/blob/master/img/capexopex.jpg" alt="My Images"></p>

CapEx and OpEx represnet two approaches to how you make an investiment which time and money

* **Capital Expenditure (CapEx)** - refers to the money a company spends towards fixed assets such as the purchase, maintenance, and improvement of buildings, vehicles, equipment or land.
    * Spend money upfront
    * Upfront cost for the company
    * Value reduced over time (tax)

* **Operational Expenditure (OpEx)** - funds that are support your day-to-day business.
    * No upfront cost
    * Pay as you use
    * Same year tax deduction

## Economies of Scale 💰

* Ability to operate more efficienlt or at a lower-cost /unit when operating at a larger scale.
* By using Azure Cloud Computing, you can achieve a lower variable cost than you can get on your own.

## Azure Global Infrastructure 🗺️

<p align="center">
<img src="https://github.com/H0j3n/Azure-AZ-900-Notes/blob/master/img/map.png" alt="My Images"></p>

* **Regions** - A set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network.
    * Each region is part of single geography and specific service availability, compliance and data residency apply.
* **Availability Zones** - Physically separate datacenters within an Azure region with independent power, network and cooling.
    * Its a good idea to user Azure Avaiability Zones when deploying highly available or mission-critical apps.
* **Geographies** - A discrete market, typically containing two or more regions that preserves data residency and compliance boudaries.
* **Region Pairs** - Providing business continuity and disaster recovery (in the cloud)
    * Helpful when an entire Azure Region goes down

## Azure Management Interfaces 🖥️

Azure provides multiple options to interact with Azure Cloud Platform:

* **Azure Portal** - Graphical User Interface for accessing a wide range of Azure Cloud Services and manage compute, storage and cloud resources. [Link to Portal]("https://portal.azure.com")

* **Azure Command Line Interface (CLI) & Azure PowerShell Module** - Cross-platform options (Windows, Mac & Linux) thath enable you to connect to your Azure Cloud account and manage reources from CLI. This could optimise and optimize your work trough scripts.

* **Azure Cloud Shell** - Offers browser-accessible, pre-configured shell experience for managing Azure resources wihtout installing, versioning and maintaining a machine yourself. It is your Microsoft-managed admin machine in Azure. Also [Link to Access]("https://shell.azure.com")

* **Azure SDKs** - Collections of libraries for programming languages. Which can help you build applications that manage and interact with Azure services and an interesting option for Developers.

* **Azure Mobile App** - Available in Apple and Google Play Stores. Can Monitor the health and status of your Azure resources, Quickly diagnose and fix issue and can run commands to manage your Azure resources.



# References

[1] https://azure.microsoft.com/en-us/overview/what-is-cloud-computing/

[2] https://azure.microsoft.com/en-us/overview/what-are-private-public-hybrid-clouds/

[3] https://medium.com/@karansinghreen/what-is-the-difference-between-public-private-and-hybrid-cloud-a41bba631479

[4] https://medium.com/@Albihany/true-cloud-story-about-iaas-paas-saas-47cfea883271

[5] https://www.bmc.com/blogs/capex-vs-opex/