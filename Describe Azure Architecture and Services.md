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
