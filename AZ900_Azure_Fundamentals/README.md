# Defining Cloud Computing
Starting point for a career in Azure
Fundational Cloud Concepts 
What is cloud computing ?
=> Delivery: Help people access computing services (servers, storage, databases, etc.), over the internet ("the cloud"), on demand
=> Advantages: Do things better and faster, server instant, scale up and down, greater flexibility
=> Cost efficiency : lower operating costs, greater effiiciency, scale as business needs change

Shared responsibility Model
- Clarification of roles and responsibility: Efficiency and convenience, Data privacy, Flexibility, Defined roles

Cloud provider is rsponsible : Physical hosts, network, datacenter
Customer is always reponsible : information and data, devices, accounts and identities

Saas: Most of the responsibilities goes to the cloud vendor
Paas : Responsibilities are shared between customer and cloud vendor
Iaas : Responsibilities is mainly on customer
On-prem : Full to Customer

Private cloud : only for one company=> quite costly because every hardware is on the head of the company <= Less flexible <= Similar to On-prem.

Public cloud : No upfront investment | vendor is responsible for hardware, full control and privacy, a lot of maintenance + upfront costs, more flexibility, available to anyone

Hybrid cloud : combine with public cloud (privare connectivity VPN / Maintain control in private cloud/on-premises), more complexity, the most flexibility, connect public workloads to private conections

## Economy of Cloud Computing
CapEx (Investissement initial pour une infrastructure physique)
=> Forecasting long term needs/value (not scalable)

OpEx (Pay as you go - Pas d'investissement initial - location de services) no need to forecast for long term needs.

Cloud model: consumption based : pay based on immediate usage, low usage = low costs, can increase resources if needed

Exam tips :
1. The cloud is on-de,and delivery of compute services over the internet
Flexibility is the key advantage
2. Ongoing, foundational topic separation of responsibility between vendor and customr

# Cloud Service Types
=> As a service (aas) brand cloud products
Trois types de clouds:
=> Difference stays in the control the customer want to keep

## Iaas: 
Infrastructure  (More responsability to the customer) : Basic computing infrastructure/Greater customization/control, pay for what you allocate, more management overhead

Responsibility of the cloud provider:
Physical Datacenter
Network cabling
Physical servers

Customer responsibility:
- Software OS updates
- User management
- Network access

- provisioned and managed over the internet

Pay-as-you-go managed IT infrastructure:
VM (servers) (Vrtual computer) => Networking, Operating Systems

Single physical sever (hypervisor) hosting multiple/individual VMs (Example: Hyper-V, VMware)

You manage a single VM that is only for you

All the VMs on the hypervisor are completely isolated from each other

## PaaS: 
Platform : prepackaged cloud services, emphasis on application development, pay for what you use, less management overhead

Responsibility of the cloud provider:
Physical Datacenter
Network cabling
Physical servers
Operating System
Development tools/Database management/Business Analysis
Server infrastructure
Auto-scaling
Software licenses/middleware

Managed Development/Deployment Services:
-> Managed services for developing solutions
Develop applications/solutions without managing infrastructure
Cloud vendor focuses on infrastructure - you focus on developing solutions

Paas Terminology: Fully managed

Serverless : 
Cloud vendor handles OS; runtime environments
Just run code
Don't worry about where it runs
Charged when code runs
Run code with no infrastructure management

## Saas: 

Software (least amount of gestion), ready-to-use applications, focus is on end-user experience, pay for what you subscribe, minimal management overhead

Responsibility of the cloud provider:
Physical Datacenter
Network cabling
Physical servers
Operating System
Development tools/Database management/Business Analysis
Server infrastructure
Auto-scaling
Software licenses/middleware
Hosted applications

Customer responsibility:
Accounts and identities (authentication requirements)
Device management (ensure device security)
Informaton and data (protect data access, access control)

Cloud-based applications:
applications hosted and accessed over the internet
subscription pricing model
Examples: email, office tools, CRMs
(Example )

Saas applications are powered by Iaas/Paas services
Benefits :
- Ready to go software (easy scaling, pre-configured and easy to use)
- Accessed over internet (no hosting required, access from anywhere)
- easy licensing (subscription model)
- Tailored for specialized use cases

## Defense in Depth
slow or stop unauthorized data access
7 layers to protect data:
- Physical security (first line of defense, building/hardware access)
- Identity access (securing identities, grant account access to only what's needed)
- Perimeter (protect against network-based attacks)
- Network (secure connectivity between resources)
- Compute (secure VMs, endpoint protection/OS patching)
- Application (resolve application vulnerabilities, secure secrets, design for security)
- Data (primary target, databases, disks, saas applications, control access)

## Exam tips : Cloud service types
Iaas : Managed infrastructure / Virtual machines (VMs)
CPU/RAM/OS/networking
Full control but with more responsibility

Paas: Fully managed cloud solutions
Cloud vendor handles infrastructure, you focus on developing soutions
Serverless:zero resource management
trade less flexibility/control for less management

Saas: Ready-to-go, cloud based software
Productivity applications:
- accessed over the internet
- hosting and scaling provided

subscription model

Defense in depth: Defend data with layers of defense : Data/application/compute/network/perimeter/identity and access/physical security

Cloud vendor handles physical security

# Cloud Benefits