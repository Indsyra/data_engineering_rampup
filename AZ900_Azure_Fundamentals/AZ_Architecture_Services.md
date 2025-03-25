# Architectural Components of Azure
## Azure Regions
### Understanding Regions
Where is Azure ?
How is it physically organized ?

Microsoft def: region is a set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network.

Set of datacenters
Latency-defined perimeter

Geographically distributed groups of datacenters

two or more data centers not too far from each other connected with a high speed connection

some regions have a single datacenter

Multiple regions strategically located worldwide

### Connectivity
Microsoft Private global Fiber Network

### Example West US 3
Multiple datacenters grouped together
each datacenter is independent from each other

### How to choose a region
You can select the region for deploying Azure resources
- Location : Choose a region closest to your users to minimize latency
- Features : Some features aren't in all regions
- Price : The price of services varies from region to region

You will often have to choose which is the most important among all of them

### Region Pairs
Two closely linked regions for redundancy and replication => High availability
Exist to provide an extra layer of protection against unexpected events

- Each Region is Paired (except Brazil South Region)
- Outage Failover
- Planned Updates
- Replication

### Sovereign regions
Isolated regions ensuring government compliance within specific jurisdictions
- Not part of Azure public cloud
- Approval required to join
- Not all services available

Azure for US Government
Azure China

### Azure for US Government
Meets higher compliance requirements
A cloud for mission accross data classifications
Eligibility : US government entity or solutions provider (federal, state, local or tibal governments, government contractors)

### Azure China
Isolated regions required for Azure workloads in China
Operated by third-party provider (21Vianet)
Data stays in China's datacenter to ensure compliance
Requires business presence in China

## Availability Zones
### What are Availability Zones ?
Physically separate datacenters within an Azure region
- Physical Location : 1+ contained datacenter within a region
- Independent : Each zone has its own power, cooling and networking
- Zones : Minimum of three zones

### Visual representation
![alt text](image-45.png)

### Regional Availability
Not all regions have availability zones
At least one zone-enabled region per country with Azure presence
More zone availability becoming available

### Using Availability Zones
Goal : Redundancy within a region
Solution/service replicated across multiple zones

If one zone goes down, service still operational.

Methods :
- Zonal services : Associate a resource with a specific zone (Example : Deploy a VM to Zone 2)
- Zone redundant services : Service automatically replicates across zones (Zone-redundant storage account)

Duplicating services accross zones come with additional costs.

## Exploring Azure Global Infrastructure
Explore : https://datacenters.microsoft.com/


### 
### 
### 
### 
### 
### 
### 
### 
### 

## Resource Organization
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Resource Hierarchy
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Exam tips
### 
### 
### 
### 
### 
### 
### 
### 
### 


# Azure Compute
## Azure Compute Concepts
Covers both Iaas and Paas

### Defining Compute
On-demand computing service that provides computing resources (disks, processors, memory, networking and OS)

Engine running your code/applications on Azure

### Azure Compute Options
Different options for different requirements

Iaas : VM
Paas : Azure App Service, Azure Functions, Azure Container Instances, Azure Kubernetes Services

### Revisiting Iaas vs Paas
Flexibility vs Management Overhead
Iaas : Greater customization/control, more managment overhead
Paas : Less customization/control, less management overhead

## Virtual Machines
### What is a VM?
Customizable, scalable and on-demand server
=> Iaas
=> Virtualized server : hosted on underlying hypervisor, full control over it, run almost any application
=> Windows or Linux servers syste,s

### Components
- CPU/Memory
- Disk
- Networking
- Operating System (Linux or Windows)
- Network controls (firewall)

### VMs and networking
All VMs must be deployed to a Network
=> Virtual network (VNet)
Not possible to create a VM without assigning it to a network
Includes one or more subnets
VM assigned private and public IP address(es) : private requires, public optional; attached to network interface card (NIC)

### Configuration
- Choose CPU, RAM and Disk Configurations
VM Size = Preconfigured CPU/RAM combinations
- Optionally, GPU and Disk types
- VM Sizes grouped into series (Examples: A series, B series, D series) : different series for different use cases
- Configure Disks (various sizes)

### Description of VM series
![alt text](image-46.png)

### VM Pricing
Different pricing for different components
CPU/RAM (Compute)
- Priced by the minute
- More compute = higher costs
- Deallocated (stopped) VMs not charged for compute

Disks
- Charged whether VM is running or not

Licensed OSs
- Windows, Red Hat, etc
- Pay-as-you go license charged same as Compute

Public IP Address(es)
- Charged by the hour
- Pricing model depends on SKU
Dynamic: No charge when VM deallocated
Static: charged regardless of VM state

### Use cases for VMs
Pros:
- Control : use VM when you need to control all aspects of an environment or machine
- Application Compatibility : Install specific applications on your Win or Linux machines, better legacy support
- Existing infrastructure : existing resources and VMs can be moved to Azure from on-premises or another cloud provider. "Lift and Shift"
- Testing and development : quickly and easily test applications and configurations, when done, simply delete the VM
- Extend your datacenter : extend your on-premises servers to work with Azure VMs, hybrid cloud.

Cons:
- More stuff to manage : much more management overhead, OS updates, patches, user control, software environments
- Higher costs : Specialize services for cloud-native applications often cost less
- Complexity in Scaling : scaling is often a more manual process

### Creating VMs
Resource organization
Required region to assign
Options
Open ports

Available in Quick Launch or search for VMs in search bar

Create a VM
Must assign to : region, resource group, network
Options : VM size, OS, Disks, and much more

Basics
- Subscription
- Resource group
- VM name
- Region
- Availability options (not required) => no infrastructure redundancy required
- Availability zone
- Security type (optional)
- Image : OS on which VM will be running
- Size : Number of CPU/Memory coniguration (B series, the cheaper one, general purpose|)
- Username
- Password
- Authentication type (for Linux only) : SSH public key or passwords
- Public inboung ports
- Select inbound ports

Disks
- Later on

Networking
- Virtual network
- Subnet
- Public IP (optional)
- NIC network security group (optional)
- Public inbound ports
- Select inbound ports

Management
- Enabling Microsoft Defender for cloud
- Login with Azure AD

### Connecting to VMs
Windows RDP port 3389
Linux SSH port 22

Windows:
- RDP : Remote Desktop
- 4 more ways to connect : Bastion basic or standard, Windows admin center, Native SSH, Serial console

Linux :
- SSH using Azure CLI : easy connect method
- Native SSH

### 
### 
### 

## Deploying your first Azure VM
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Virtual Machine Scale Sets
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Availability Sets
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Azure Virtual Desktop
### 
### 
### 
### 
### 
### 
### 
### 
### 

## App Services
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Azure Functions
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Introduction to Containers
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Container Deployment Options
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Exam Tips
### 
### 
### 
### 
### 
### 
### 
### 
### 


# Azure Networking
## Virtual Networks
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Network Security
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Creating Virtual Networks
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Network Peering
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Azure DNS
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Hybrid Networking
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Azure VPN
### 
### 
### 
### 
### 
### 
### 
### 
### 

## ExpressRoute
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Public and Private Endpoints
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Exam Tips
### 
### 
### 
### 
### 
### 
### 
### 
### 


# Azure Storage
## Introduction to Azure Storage
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Azure Blobs
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Blob Storage Tiers
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Creating an Azure Storage Account and Blob Container
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Disks
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Azure Files
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Tables and Queues
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Storage Redundancy
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Moving Data in Azure Storage
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Additional Migration Options
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Premium Performance Options
### 
### 
### 
### 
### 
### 
### 
### 
### 

## Exam Tips
### 
### 
### 
### 
### 
### 
### 
### 
### 
