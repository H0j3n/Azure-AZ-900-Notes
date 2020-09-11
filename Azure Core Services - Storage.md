# Azure Core Services - Storage


## Azure Storage

* Azure Storage is Microsoft's cloud storage solution for modern data storage scenarios.

**Data Serviecs**

* **Azure Blobs (Unstructured Data)** - Scalable Object Store
    - Azure Blob Storage is Microsoft's object storage solution for the cloud, optimized to store massive amounts of unstructure data (text or binary data)
    - BLOB (Binary Large Objects)
    - Suitable for storing images and files, stream video and audio, log files and store data for BKP and restore (DR)
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

# References

1. https://azure.microsoft.com/en-us/services/storage/blobs/