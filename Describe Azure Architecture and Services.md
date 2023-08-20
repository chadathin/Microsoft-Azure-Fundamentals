## Getting started with Azure accounts
To create and use Azure services, you and Azure subscription. After you've created and Azure Account, you can create additional subscriptions. 
- For example, your company might use a single Azure account for your business and separate subscriptions for development, marketing, and sales departments. 
- After you've created an Azure subscription, you can start creating Azure resources within each subscription.
## Describe Azure's Physical Infrastructure
- **Regions**: A geographical area on the planet that contains at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network. 
- **Availability Zones**: Physically separate dataacenters within an Azure region. Each availability zone is made up of one or more datacenters equipped with independent power, cooling and networking.
- An Availability zone is set up to be an isolation boundary. If one zone goes down, the other continue working. Availabilty zones are connected through high-speed, private fiberoptic networks.
- Availability zones are primarily for VMs, managed disks, load balancers, and SQL databases. Azure services that support availability zones fall into three categories:

1. Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
2. Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).
3. Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.

- **Region Pairs**: Most Azure regions are paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away. This approach allows for the replication of resources across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect an entire region.

## Describe Azure management infrastructure


## Azure VMs
- Provided as IaaS.
- Up to User to keep apps and software up to date.

## Azure containers
- Azure Container Instances are provided as a PaaS
- **VM's** virtualize the _hardware_, **containers** virtualize the _operating system_
- Azure Container Apps are also a PaaS offering
- Azure Kubernetes Service (AKS) is a container orchestration service. Orchestration services manage the lifecycle of containers. When you're deploying a fleet of containers, AKS can make fleet management simpler and more efficient.

## Azure Functions
- SaaS offering
- Event-driven, serverless computer option
- Does not require maintaining virtual machines or containers (cloud provider does all that)
- An event wakes the function, alleviating the need to keep resources provisioned when there are no events
- Only pay for the CPU usage while functionl is running
- Resources allocated when function is triggered, deallocated when the function is finished
- Can be stateless (run anew every time) or stateful (relies on context to track prior activity)

## Application hosting options
- **Azure App Service**
	- Enables users to build and host web apps, background jobs, mobile back-ends and RESTful APIs in the programming language of their choice without managing infrastructure
  - Automatic scaling and high availability
  - Supports Windows and Linux
  - Enable automated deployments from GitHub, Azure DevOps or any Git repo to support a CD model
  - HTTP-based service
  - Supports multiple languages including .NE, .NET Core, Java, Ruby, Node.js or Python
- **Types of app services**
	- Web apps, API apps, WebJobs, Mobile apps

## Azure Virtual Networking

## Describe Azure Storage Redundancy
- Redundancy in the primary region: Data in an Azure Storage account is always replicated three times in the primary region. Azure Storage offers two options for how your data is replicated in the primary region: **Locally Redundant Storage (LRS)** or **Zone-Redundant Storage (ZRS)**.
- **Locally Redundant Storage (LRS)** replcates your data three times within a single data center in the primary region. LRS provides at least 11 nine of durability (99.999999999%) of object over a given year.
  - LRS is the lowest-cost redundancy option and offers the least durability compared to the other options. LRS protects your data against server rack and drive failures. However, if a disaster such as a fire or flood occurs within the data center, all replicas of a storage account using LRS may be lost or unrecoverable.  To mitigate this risk, Microsoft recommends using **Zone-Redundant Storage (ZRS)**, **Geo-Redundant Storage (GRS)**, or **Geo-Zone-Redundant Storage (GZRS)**.

- **Zone-Redundant Storage (ZRS)**: For Availability Zone-enabled Regions, zone-redundant storage (ZRS) replicates your Azure Storage data synchronously across three Azure Availability zones in the primary Region. (One copy per Availability Zone). ZRS offers durability for Azure Storage data objects of at least 12 nines (99.9999999999%) over a given year.
  - With ZRS, your data is still accessible for both read and write operations, even if a zone becomes unavailable. No remounting of Azure file shares from the connected clients is required. If a zone becomes unavailable, Azure undertakes netwroking updates, such as DNS repointing. These updates may affect your application if you access data before the updates have completed. 
  - Microsoft recommends using ZRS in the primary region for scenarios that require high availability. ZRS is also recommended for restricting replication of data within a country or region to meet data governance requirements.
- **Redundancy in a Second Region**
  - For applications requiring high durability, you can choose to additionally copy the data in your storage account to a secondary region that is hundreds of miles away from the primary region.
  - When you create an Azure Storage account, you select the primary region for the account. The paired Secondary Region is based on _Azure Region Pairs_ and cannot be changed.
  - Two options:
    - **Geo-Redundant Storage (GRS)**: Similar to running LRS (locally Redundant Storage) in two regions. 
    - **Geo-Zone-Redundant Storage (GZRS)**: Similar to running ZRS (Zone Redundant Storage)  in the primary region and LRS in the secondary region.
  
  - **Geo-Redundant Storage (GRS)**
    - Copies your data asynchronously three times withint a single physical location, in the primary region using LRS. It then copies your data asynchronously to a single physical location in the secondary region (the region pair) using LRS. GRS offers durability for Azure Storage data objects of at least 16 nines (99.99999999999999%) over a given year.

  - **Geo-Zone-Redundant storage**
    - GZRS combines high availability provided by redundancy across availability zones with protection from regional outages provided by geo-replication. 
    - Data in a GZRS storage account is copied accross three Azure availability zones in the primary region (similar to ZRS) and is also replicated to a secondary geographix region (using LRS) for protection from regional disasters.
    - Microsoft recommends using GZRS for applications requiring maximum consistency, durability and availability, excellent performance and resilience for disaster recovery.
    - Also at 16 nines of durability.
  **Read access to data in the secondary region**
    - Data typically only available to be read if customer, or Microsoft, initiates a failover from the primary to secondary region.
    - BUT, if you enable readaccess to the secondary region, that data is _always_ available.
    - For read access to a secondary region, enable read-access geo-redundant storage (RA-GRS) or read-access geo-oxone-redundant storage (RA-GZRS). 