# Azure Core Services - Database


## Azure Cosmos Database

* **Azure Cosmos DB** is Microsoft's globally distibuted, multi-model database service.
* It is designed for high scale, global replication, low latency databases.
* Document Database.
* Document format JSON (Javascript Object Notation)
* **JSON** - an open-standard file format that human-readable syntax, consisting of attribute-value pairs
* **Key Features**
    - **Global distribution** -> transparent multi-region distribution
    - **Highly available (Always on)** - 99.9999%
    - **Elastic scale** -> From thousands to hundreds of millions of requests/sec around the globe
    - **Low latency guarantee** -> less than 10ms or 99% of requests
    - **No schema or index management** -> just operate on the documents, which can have different properties/formats.
    - **Multiple APIs Available**
        * SQL (Core API) - query your data just like you would do with any normal Database
        * Cassandra
        * MongoDB
        * Gremlin
        * Azure Table Storage
* **Requests units**
    - The cost of all database operations is expressed by Azure Cosmos DB in Request Units (RUs) -> read, insert, delete, query
    - Simply put, just think of RUs per second as the currency for throughput
    - You don't pick how much CPU, RAM, etc you only pick one aggregate measure, the throughput measure, which is the RUs.
* **Partitions**
    - Items in a container are divided into distinct subsets called logical partitions.

## Azure SQL Database

* General-purpose relational database-as-a-service (DBaaS) based on the latest stable version of Microsoft SQL Server Database Engine.
* Provided as a managed service, you can create a highly available and high-performance data storage layer for the applications and solutions in Azure
* **Deployment Models**
    - **Single** - Fully managed, isolated database
    - **Elastic Pool** - Collection of single databases with a shared set of resources.
    - **Managed Instance** - Fully managed instance of SQL Server & Full SQL server capabilities 
* Azure SQL Database Server is the central administrative point for multiple single or pooled databases.
* Similar to on-prem traditional SQL server.
* **Available through 3 pricing models:**
    - **Database Transaction Unit (DTU)**
    - **Virtual Core (vCore)** - recommended
    - **Serverless model** - vCore based
* With DTU, you scale storage with compute at the same time.
* With vCore you can scale storage independently from compute
* Any existing SQL license can be used with vCore model.

## Azure Database for MYSQL 

* Azure Database for MYSQL is a relational database service based on the MYSQL Community Edition database engine
* **Benefits?*
    - Built-it high availability
    - Pay-as-you-go pricing
    - Scaling in just seconds
    - Built-in security for data at-rest and in-transit
    - Automatic bkp and point-in-time-restore up to 35 days.
    - Enterprise-grade security and compliance.

## Azure Database for PostgreSQL 

* Relational Database service based on the community version of open-source PostgreSQL database engine.
* **Deployment options**
    - Single Server
    - Hyperscale
* **Key benefits**
    - Built-in Hight Availability
    - Enterprise-grade security and compliance
    - Built-in security for data at-rest or in-motion
    - Automatic backups and point-in-time-restore up to 35 days
    - Vertical Scale as needed in seconds
* **Pricing Tier**
    - Basic
    - General Purpose
    - Memory Optimized(vCore,RAM,storage)
* As opposed to single server option, hyperscale option scales the DB horizontally (multiple machines)
* Incoming SQL queries are sent to the servers, which results in faster responses on large datasets.
* Servers are actually part of a server group, coordinator node and worker node roles are available.

## Azure Database Migration Service (DMS)

* Fully managed service designed to enable seamless migrations from multiple database sources to Azure Cloud
* Designed to support different migration scenarios for both offline (one-time) and online (continuous sync) migrations.



## References