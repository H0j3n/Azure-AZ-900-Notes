# Others Azure Core Services

## Azure Networking

* Covers a broad range of networking capabilities that can be used together or separately.
* **Provides the following key capabilities**
    - **Connectivity Services** - vNet, ExpressRoute, VPN Gateway
    - **Application protection services** - DDoS protection, Firewall, NSGs, WAF
    - **Application delivery services** - CDN, Load Balancer, Application Gateway
    - **Netwok Monitoring** - Azure Monitor, Azure Service Health, Network Watcher

## Azure Connectivity Services - Virtual Network

* **Virtual Network (vNET)** - the fundamental building block for your private network in Azure (private Data Center)
* **vNET Peering** - Communicate between each other, within the same or different Azure Regions.
* **Load Balancer** - Communicate inbound to a resource by assigning a public IP address or a public Load Balancer.
* **On Prem DC** - Connect your on-premises to a virtual network using **VPN Gateway** or **ExpressRoute**.
* **Azure Content Delivery Network (CDN)** - delivers high-bandwith content to users by caching their content at strategically placed physical nodes across the world.
* **Azure Application Delivery Services** - web traffic load balancer that enables you to manage traffic to your web applications.

## IOT

* **Azure Internet of Things (IoT)** is a collection of Microsoft-managed cloud services that connect, monitor and control billions of IoT assets.
* IoT Solution is made up of one or more IoT devices that communicate with one or more back-end services hosted in Azure Cloud.
* IoT device is typically made up of a circuit board with different sensors attached connected to the internet.
* **Azure IoT Hub**
    - Managed service that acts a a central message hub for bi-directional communication between your IoT application and the devices it manages.
* **Azure IoT Central**
    - IoT application platform that reduces the burden and cost of developing, managing and maintaining enterprise-grade IoT solutions (PaaS).
    - You can use IoT Central to create a custom, cloud-hosted IoT solution for your organization, typically consists of:
        * A cloud-based appllication that receives data from your devices and enables you to manage those devices.
        * IoT devices connected to your cloud-based application.

## Big Data and Analytics

* Deliver intelligent actions that improve customer engagement, increase revenue and lower costs.
* **Azure SQL Data Warehouse** - cloud-based enterprise data warehouse that you can use to quickly run complex queries across petabytes of data.
* Import data into **SQL Data Warehouse** and run high-performance analytics, leveraging massively parallel processing (MPP).
* More and more business are relying today on Big Data and Analytics solutions in order to extract real insights from the market and drive business in the right direction.
* **Azure Databricks**
    - Apache Spark-based analytics platform optimized for the Microsoft Azure Cloud Platform
    - Can analyze Data and generate meaningful insights.
    - **Read Data From**
        * SQL Data Warehouse
        * Azure Blob Storage
        * Azure Data Lake Storage
        * Azure Cosmos DB
* **Azure HDInsight**
    - Cost effective enterprise-grade service for open source analytics with Azure HDInsight, I would like you to think open source.
    - Run popular open source frameworks - including **Apache Hadoop, Spark and Kafka**, process massive amounts of data and get all the benefits of the broad open source ecosystem with the global scale of Azure.
    - Integrates with other Azure services, for example **Data Factory & Data Lake Storage**

## Aritifcal Intelligence & Machine Learning

* **Machine Learning** is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes and trends.
* By using machine learning, computers learn without being explicitly programmed.
* **Artifical Intelligence** is the capability of a machine to imitate intelligent human behavior.
* Azure offering -> Azure Machine Learning & Azure Machine Learning Studio (classic)
* **Azure Machine Learning Studio (Classic)**
    - Collaborative, drag and drop visual workspace where you can build, test and deploy ML solutions without needing to write code.

## DevOps

* DevOps is a set of practices that combines software development (Dev) and information-technology operations (Ops) which aims to shorten the systems development life cycle and provide continous delivery with high software quality.
* DevOps is the union of people, process and products to enable continous delivery of value to our customers.
* With DevOps you deploy code more frequently, reduce lead time, reduce change failure rate.
* Azure DevOps provides several tools you can use for better team collaboration.
* Suite of services that provide a solution to anyone who wants a tool to create a step-by-step production and continious improvement chain.
* **Azure Tools**
    - **Azure Boards** - These are agile tools that help us plan,track and discuss our work even with other teams
    - **Azure Pipelines** - These will let us build,test and deploy with CI/CD that works with any language, platform and cloud.
    - **Azure Test Plans** - These are manual and exploratory testing tools.
    - **Azure Repos** - These provide unlimited, cloud-hosted private and public Git repos.
    - **Azure Artifacts** - These let us create, host and share packages.
* **Azure DevTest Labs**
    - Enables developers to efficiently self-manage virtual machines (VMs) and PaaS resources without waiting for approvals.
    - With Azure DevTest Labs developers become autonomous and can create labs consisting of pre-configured resources.
    - You can easily test the latest versions of your applications and speed up the process of creating and terminating the testing environments.

# References