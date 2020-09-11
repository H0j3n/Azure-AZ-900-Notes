# Azure Core Services - Storage


## Azure Storage

* Azure Storage is Microsoft's cloud storage solution for modern data storage scenarios.

**Data Serviecs**

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

* **Azure Files (SMB File Share)** - Managed File Share
    - Offers fully managed file shares in the cloud that are accessible via SMB protocol.
    - Can be mounted (attached) by both on-permises and cloud machines.
    - Applications can mount a file storage share to access file data, just as a desktop application would mount a typical SMB share.
* **Azure Queues** - Messaging Store
    - Service for storing large numbers of messages, accesible from anywhere in the world.
    - A messaging store for reliable messaging between application components.
    - When app components are decoupled, they can scale independently,
    - Queue Storage provides asynchronous message queueing for communication between application components.
* **Azure Tables** - NoSQL Structured Data 
    - Service that stores strucued NoSQL data in the cloud.
    - Azure Table storage stores large amounts of structured data, known as NoSQL datastore. 
    - Ideal for storing structured, non-relational data.
    - **Azure managed service** - tables will scale as demand increases.

## Azure Data Lake Storage Gen2

* Built using two existing services -> Azure Storage & Azure Data Lake Storage Gen1
* Provides big data analytics capabilities, built on Azure Storage and stores both structured and unstructured data.
* Scalabe (up to exabytes o data = 1m TB), cost effective (Blob storage lifecycle and access tiers)

# References

1. https://azure.microsoft.com/en-us/services/storage/blobs/