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
