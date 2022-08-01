## Objective 1 - Cloud concepts

### Cloud Models - Objective Domain

- `Cloud computing`
  Is the delivering of computing services over the internet, enabling faster innovation, flexible resources and economies of scale.

- `Public cloud`
- - Owned by cloud services os hosting provider
- - Provides resources and services to multiple organizations and users
- - Accessed via secure network connection (typically over the internet)

- `Private cloud`
- - Organizations create a cloud environment in their datacenter
- - Organization is responsible for operating the services they provide
- - Does noite provide access to users outside of the oraganization

- `Hybrid cloud`
- - Combines **Public** and **Private** clouds to allow applications to run in the most appropriate location.

| Cloud model   | Comparison                                                                                                                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Public cloud  | - No capital expenditures to scale up <br/> - Applications can be quickly provisioned and deprovisioned <br/> - Organizations pay only for what they use                                                     |
| Private cloud | - Hardware must be purchased for start-up and maintenance <br/> - Organizations have complete control over resources and security <br/> - Organizations are responsible for hardware maintenance and updates |
| Hybrid cloud  | - Provides the most flexibility <br/> - Organizations determine where to run their applications <br/> - Organizations control security, compliance, or legal requirements                                    |

### Cloud Benefits - Objective Domain

- High availability
- Scalability
- Global reach
- Agility
- Disaster recovery
- Fault tolerance
- Elasticity
- Customer latency capabilities
- Predictive cost considerations
- Security

### Compare CapEx vs. OpEx

| Capital Expenditure (CapEx)                                                                                          | Operational Expenditure (OpEx)                                                       |
| -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| The up-front spending of money on physical infrastructure <br/> Costs from CapEx have a value that reduces over time | Spend on products and services as needed, pay-as-you-go <br/> Get billed immediately |

### Consumption-based model

Cloud service providers operate on a consumption-based model, which means that end users only pay for the resources that they use. Whatever they use is what they pay for

- Better cost prediction
- Prices for individual resources and services are provided
- Billing is based on actual usage

### Cloud Services - Objective Domain

- `Infrastructure-as-a-Service _(IaaS)_`

Build pay-as-you-go IT infrastructure by renting servers, virtual machines, storage, networks, and operating systems from a vloud provider.

- `Plataform-as-a-Service _(PaaS)_`
  Provides environment for building, testing, and deploying software applications, without focusing on managing underlying infrastructure

- `Software-as-a-Service _(SaaS)_`
  User connect to and use cloud-based apps over thw internet: for example, Microsoft Office 365, email, and calendars.

- `Hybrid cloud`
- - Combines **Public** and **Private** clouds to allow applications to run in the most appropriate location.

| Iaas                                                                                             | Paas                                                                                        | Saas                                                                                          |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| The most flexible cloud service <br/> You configure and manage the hardware for your application | Focus on application development <br/> Platafor management is handled by the cloud provider | Pay-as-you-go pricing model <br/> Users pay for the software they use on a subscription model |

![Shared resposibility model](../img/Shared_responsibility_model.jpg)

![Pizza shared resposibility model](../img/Pizza_shared_responsibility.jpg)

### Serveless computing

With **serveless computing applications**, the cloud service provider automatically provisions, scales, and manages the infrastructure required to run the code.

- **Azure functions** is code running your service and not the underlying plataform or infrastructure. It creates infrastructure based on a event.
- **Azure Logic Apps** is a cloud service that helps you automate and orchestrate tasks, business processes, and workflows when you need to integrate apps, data, systems and services.

### Objective 1 - Review

- Microsoft offers Public, Private and Hybrid cloud models so you can build based on your needs.
- From high-availability to elasticity to disaster recovery to pay-as-use, the benefits of the Azure cloud are numerous.
- IaaS, Paas, SaaS and serveless, or a combination.
- Shared responsibility.

### Kwnowledge check

---

**Which cloud service type requires the customer to manage the underlying hypervisor plataform for their cloud deployments?**

- Infrastructure-as-a-Service
- Plataform-as-a-Service
- Software-as-a-Service
- `None of the above`

> **Note**: The hypervisor is part of the host system. Whe we see something like this, we're talking about the actual host.

---

**Which `cloud service type` would best match the following situation?**

Several web applications have been developed internally in your organization. The web applications allow users to enter details in a forma and those details are then emailed to a shared mailbox. The form is acessible from the internet and can be accessed anonymoulsy.

`Plataform-as-a-Service (PaaS)`

because the web applications are publicly accessible and do note require authentication, a PaaS service that allows customers to host web sites without having to manage servers would be best.

The websites can be deployed quickly and will have publicly accessible endpoints with minimal configuration.

## Emails could be sent using a `SaaS` solution as well.

**Which `cloud deployment model` would best match the following situation?**

A server is needed to process data for a short-term project. The organization does not have hardware that meets the perfomance requirements or any available staff to deploy it. The project starts in a few days and the server is not needed when the project is completed.

`Public cloud`

Because the server is only needed for a short time, public cloud would be the best option.

Creating a server in the public cloud will be cost-effective with pay per-usage billing and the resource can be removed when the project is complete.

A `PaaS` database could also be a candidate, eliminating the need for a server.

---

**The capability of a system to be enlarged to accommodate a growing amount of work is best described by the term?**

- Reliability
- Elasticity
- `Scalability`
- Agility

---

**In general terms, when an organization moves to the cloud will it see a reduction in CapEx, OpEx, or both?**

`Both`. Quite often, and immediate reduction in CapEx is realizaed by moving to the cloud. This can be through the immediate reduction in on-premises components by eliminating or migrating workloads.

Organizations can also see a reduction in the OpEx through the reduced time and hours spent on IT maintenance. Organizations that move to the cloud see a significant reduction in IT management tasks as responsibilities shift to the cloud provider.

---

## Objective 2 - Core Azure Services

### Core Azure architectural components - Objective Domain

#### **Regions**

Azure offers more global regions tha any other cloud provider with 60+ regions representing over 140 countries

- Regions are madeup of one or more datacenters in close proximity.
- Provide flexibility and scale to reduce customer latency.
- Preserve data residency with a comprehensive compliance offering.

##### **Regions pairs**

- At least 300 miles of separation between region pairs.
- Automatic replication for some services.
- Prioritized region recovery in the event of outage.
- Updates are rollout sequentially to minimize downtime.

![Geographies](../img/Geographies.jpg)

#### **Availability zones**

- Provide protection against downtime due to datacenter failure.
- Physically separate datacenters within the same region.
- Each datacenter is equipped with independent power, cooling and networking.
- Connected through private fiber-optic networks.

### Azure Resources

Azure resources are components like storage, virtual machines and networks that are available to build cloud solutions.

- Virtual Machines
- Storage Accounts
- Virtual Networks
- App Services
- SQL Databases
- Function

#### Resource groups

A resource group is a container to manage ad aggregate resources in a single unit.

- Resources can exist in only one resource group
- Resources can exist in different regions
- Resources can be moved to different resource groups
- Applications can utilize multiple resource groups

#### Azure Resource Manager (ARM)

Provides a management layer that enables you to create, update and delete resources in your Azure subscription.

### Objective 2 - Review

- a

### Kwnowledge check

---

**Which cloud service type requires the customer to manage the underlying hypervisor plataform for their cloud deployments?**
