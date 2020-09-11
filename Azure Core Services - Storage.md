# Azure Core Services - Storage


## Azure Storage

* Azure Storage is Microsoft's cloud storage solution for modern data storage scenarios.

## Data Serviecs

* **Azure Blobs (Unstructured Data)** - Scalable Object Store
    - Azure Blob Storage is Microsoft's object storage solution for the cloud, optimized to store massive amounts of unstructure data (text or binary data)
    - BLOB (Binary Large Objects)
    - Suitable for storing images and files, stream video and audio, log files and store data for BKP and restore (DR)
    - World wide reable, only internet connetion is needed (Blobs accessed through HTTP/S)
    - Highly scalable Azure service can support thousands of connections, massive amount of data.
    - Azure Blob Storage supports Azure Data Lake Storage Gen2
    - This is Microsoft's data analytics solution for the cloud
    - **Azure Blob Storage Lifecylce & Access Tiers**
        * Azure Storage offers 3 access tiers -> Hot (frequently accessed data), Cool (infrequently access data - stored min 30 days) and Archive (rarely access data - stored min 180 days.)
        * Multiple access tiers available, we can build a storage lifecycle policy which translates to cost-effective storage.
        * Policy -> **HOT => COOL => ARCHIVE**
    - **Azure Storage Encryption**
        * Automatically encrypt your data in Azure Cloud.
        * Done using :
            - **Microsoft-managed encryption keys (Azure Storage Service Encryption - SSE)**
            - **Customer Encryption Keys (client-side encryption)**
    - **Azure Storage Replication**
        * Always replicate data in your storage account to ensure durability and high availability.
        * Data can be replicated within the same Data Center, accross zonal Data Centers within the same region or accross geographically separated regions.
        * Multiple redundancy options exist, can be selected when storage account is created.
        * **Locally Redundant Storage (LRS)** replicates your data three times within a single data center.
        * **Zone-Redundant Storage (ZRS)** replicates your data across three storage clusters in a single region (3 AZs)
        * **Geo-Redundant Storage (GRS)** replicates data to a secondary region (min 300 miles away)
        * **Read Access Geo Redundant Storage (RA-GRS)** provides read-only access to the data in the secondary location, in addition to geo-replciation accross two regions (GRS)
        * **Geo-zone-redundant Storage (GZRS)** combines ZRS and GRS, data in 3AZs (1st region) and in a (2nd region)
        * **Read-Access GZRS (RZ-GZRS)** enables read access to data in the secondary region.

* **Azure Files (SMB File Share)** - Managed File Share
    - Offers fully managed file shares in the cloud that are accessible via SMB protocol.
    - Can be mounted (attached) by both on-permises and cloud machines.
    - Applications can mount a file storage share to access file data, just as a desktop application would mount a typical SMB share.
    - Traditional file servers can be replaced with Azure Files or additional capacity can be added
        * Azure File Shares can be mounted from any location
        * Works on Windows, Mac and Linux
    - Lift and shift the Apps
        * Both the app and the data in Azure
        * App on-perm and data in Azure Files
    - Plug and play compatibility - SMB industry standard
    - **Managed Service** - Azure takes care of hardware and software updates, necessary upgrades and system patching.
    - **Automate work** 
        * Multiple tools available for scripting
        * Azuer CLI, Powershell
    - Always-on File Share
        * High Available , highly scalable
        * No maintenance windows, planned or unplanned.
* **Azure Queues** - Messaging Store
    - Service for storing large numbers of messages, accesible from anywhere in the world.
    - A messaging store for reliable messaging between application components.
    - When app components are decoupled, they can scale independently,
    - Queue Storage provides asynchronous message queueing for communication between application components.
    - **Queue** - container of messages
    - **Message** - Data in any format
    - Independent queues, separate business purpose.
* **Azure Tables** - NoSQL Structured Data 
    - Service that stores strucued NoSQL data in the cloud.
    - Azure Table storage stores large amounts of structured data, known as NoSQL datastore. 
    - Ideal for storing structured, non-relational data.
    - **Azure managed service** - tables will scale as demand increases.
    - Highly scalabale and very cheap Azure Storage service, NoSQL database for everyday need and serverless apps.
    - Stores structured NoSQL data in the cloud, providing a key/attribute store with a schemaless design.
    - Key/Attribute -> Tags (name/value)
    - **Schemaless** - database doesn't have fixed data structure.
    - **Storage Account**
        * Multi-purpose storage service
        * Process up to 20,000 rows/s
    - **Table**
        * Collection of rows (entity)
        * Process up to 2000 rows/s
    - **Entity**
        * Collection of properties (columns and values)

## Azure Data Lake Storage Gen2

* Built using two existing services -> Azure Storage & Azure Data Lake Storage Gen1
* Provides big data analytics capabilities, built on Azure Storage and stores both structured and unstructured data.
* Scalabe (up to exabytes o data = 1m TB), cost effective (Blob storage lifecycle and access tiers)


## Azure Managed Disks Introduction

* Azure managed disks are block-level storage volumes that are managed by Azure and used with Azure VMs.
* Azure will manage the storage account for you that will store the *.VHD file.
* You only need to specify the disk size, the disk type and provision the disk.
* Options => Standard HDD/SSD, Premium SSD, Ultra Disks
* **Roles**
    - OS Disk (Windows, Linux) - pre-installed OS
    - Temporary disk - short-term storage, data persists a VM reboot, power off (data is lost)
    - Data disk - persistent data
* **Benefits**
    - Highly Durable and Highly Available
        * 99.999% Availability
        * 99.9999999999 (11 9's) -> Locally Redundant Storage
        * 99.9999999999999999 (16 9's) -> Geo-ZRS
    - Deploy VMs simple and highly scalable
        * 50,000 VM disks of a type in a subscription per region.
    - Fully integrated with availability sets
        * Disks are isolated from each other to avoid a single point of failure (SPOF)
    - Fully integrated with availability zones
        * Disks are isolated from each other, protects you from datacenter failures.
    - Granular access control
        * Assign specific permissions for a managed disk to one or more users.

# References

1. https://azure.microsoft.com/en-us/services/storage/blobs/