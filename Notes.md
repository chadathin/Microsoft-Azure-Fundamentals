## Define cloud computing.
- Cloud computing is the delivery of computing services over the internet. Computing services include common IT infrastructure such as virtual machines, storage, databases, and networking. Cloud services also expand the traditional IT offerings to include things like Internet of Things (IoT), machine learning (ML), and artificial intelligence (AI).

## Describe the shared responsibility model.
- With the shared responsibility model, these responsibilities get shared between the cloud provider and the consumer. Physical security, power, cooling, and network connectivity are the responsibility of the cloud provider. At the same time, the consumer is responsible for the data and information stored in the cloud. (You wouldn’t want the cloud provider to be able to read your information.) The consumer is also responsible for access security, meaning you only give access to those who need it.

- IaaS (Infrasctructure as a service): Cloud provider provides hardware and virtualization. User responsible for everything esle (Cloud provider bears least amount of responsibility)

- PaaS (Platform as a service): Cloud provider provides hardware, the operating system, virtualization, etc. The User is responsible for scaling, the app code and data & configurations. Kind of a mix of responsibility.

- SaaS (Software as a service): Cloud provider provides nearly everything. User responsible for data and configuration (Cloud provider bears most of the responsibility.)

- You’ll always be responsible for:

    The information and data stored in the cloud
    Devices that are allowed to connect to your cloud (cell phones, computers, and so on)
    The accounts and identities of the people, services, and devices within your organization

## The cloud provider is always responsible for:

    The physical datacenter
    The physical network
    The physical hosts

## Your service model will determine responsibility for things like:

    Operating systems
    Network controls
    Applications
    Identity and infrastructure


## Define cloud models, including public, private, and hybrid.
- Private: A private cloud is, in some ways, the natural evolution from a corporate datacenter. It’s a cloud (delivering IT services over the internet) that’s used by a single entity.

- Public: A public cloud is built, controlled, and maintained by a third-party cloud provider. With a public cloud, anyone that wants to purchase cloud services can access and use resources. The general public availability is a key difference between public and private clouds.

- Hybrid: A hybrid cloud is a computing environment that uses both public and private clouds in an inter-connected environment. A hybrid cloud environment can be used to allow a private cloud to surge for increased, temporary demand by deploying public cloud resources.

- MultiCloud: In a multi-cloud scenario, you use multiple public cloud providers. Maybe you use different features from different cloud providers. Or maybe you started your cloud journey with one provider and are in the process of migrating to a different provider. Regardless, in a multi-cloud environment you deal with two (or more) public cloud providers and manage resources and security in both environments.

## Describe the consumption-based model.
- CapEx: Capital Expenses; one-time, up-front expenditure to purchase or secure tangible resources. A new building, repaving the parking lot, building a datacenter, or buying a company vehicle are examples of CapEx.

- OpEx: Operating Expenses; spending money on services or products over time. Renting a convention center, leasing a company vehicle, or signing up for cloud services are all examples of OpEx.

- Consumption-based model: Only paying for what you use.
    - This consumption-based model has many benefits, including:
        No upfront costs.
        No need to purchase and manage costly infrastructure that users might not use to its fullest potential.
        The ability to pay for more resources when they're needed.
        The ability to stop paying for resources that are no longer needed.


## Security and Governance in the cloud
- On the security side, you can find a cloud solution that matches your security needs. 

- If you want maximum control of security, **infrastructure as a service** provides you with physical resources but lets you manage the operating systems and installed software, including patches and maintenance. 
- If you want patches and maintenance taken care of automatically, **platform as a service** or **software as a service** deployments may be the best cloud strategies for you.


## Describe each type of cloud service
- **IaaS (Infrastructure as a Service)**
    - the most flexible category of cloud services, as it provides you the maximum amount of control for your cloud resources. In an IaaS model, the cloud provider is responsible for maintaining the hardware, network connectivity (to the internet), and physical security. You’re responsible for everything else: operating system installation, configuration, and maintenance; network configuration; database and storage configuration; and so on. With IaaS, you’re essentially renting the hardware in a cloud datacenter, but what you do with that hardware is up to you.
    - Ex 1: Lift-and-shift migration: You’re standing up cloud resources similar to your on-prem datacenter, and then simply moving the things running on-prem to running on the IaaS infrastructure.
    - Ex 2: Testing and development: You have established configurations for development and test environments that you need to rapidly replicate. You can stand up or shut down the different environments rapidly with an IaaS structure, while maintaining complete control.

- **PaaS (Platform as a Service)**
    - Middle ground between renting space in a datacenter (IaaS) and paying for a complete and deployed solution (SaaS). 
    - In a PaaS environment, the cloud provider maintains the physical infrastructure, physical security, and connection to the internet. They also maintain the operating systems, middleware, dev tools and BI services that make up a cloud solution.
    - In a PaaS scenario, you don't ahve to worry about the licensing or patching for operating systems or databases.
    - Ex 1: **Development framework**: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. Similar to the way you create an Excel macro, PaaS lets developers create applications using built-in software components. Cloud features such as scalability, high-availability, and multi-tenant capability are included, reducing the amount of coding that developers must do.
    - Ex 2: **Analytics or business intelligence**: Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions.
- **SaaS (Software as a Service)**
    - Software as a service (SaaS) is the most complete cloud service model from a product perspective. With SaaS, you’re essentially renting or using a fully developed application. Email, financial software, messaging applications, and connectivity software are all common examples of a SaaS implementation.
    - While the SaaS model may be the least flexible, it’s also the easiest to get up and running. It requires the least amount of technical knowledge or expertise to fully employ.
    - Most reesponsibility on Cloud provider; least responsibility on User. 
    - In a SaaS environment, users are responsible for the data they put into the system, the devices they allow to connect to the system and users that have access. Nearly everything else falls on the cloud provider.
    - The cloud provider is responsible for physical security of the datacenters, power, network connectivity, and application development and patching.
    - Common examples include:
        <ol>
            <li>Email and messaging</li>
            <li>Business productivity applications</li>
            <li>Finance and expense tracking</li>
        </ol>
    
