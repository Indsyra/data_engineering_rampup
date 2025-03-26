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


## Deploying your first Azure VM
### Create a VM
From Homepage, click on create a resource.
Under "Virtual Machine", click on create

## Virtual Machine Scale Sets
### What is VMSS
Auto-scaling groups of identical VMs
Ability of create and manage multiple, load-balanced and identical VMs.

### Problem to solve
Too much load/traffic for server to handle

### How does it work
Multiple identical VMs
- Identically configured
- All managed from the same place

Behind a Load Balancer
- Directs traffic to available VMs
- Single frontend for users (e.g. a single website address)

Increase/decrease VM count
- Can automatically or manually adjust count
- Horizontal scaling

### Benefits
Multiple identical VMs: simple to manage using a load balancer
High availability : zone-redundant, deployed accross multiple zone in single region
Auto-Scaling
Large Scale : Up to 1000 VMs in a single scale set
No extra cost

### Creating Cloned VMs
From Baseline image : 
- Capture image from baseline/reference VM
- Scale Set VMs crated from captured image

Configuration script at startup
- New clone VM runs configuration script on first boot

Combination of both
- Reference image + additional configurations

## Availability Sets
### Purpose
Provides a method for high availability for static VMs in Single Datacenter/Zone

Differences compared to Scale Sets:
- Non-identical VMs
- No auto scalling
- Single datacenter/zone

### Breaking down
It provides logical grouping of VMs with separate Fault and Update Domains for high availability.

### Fault Domain
Underlying hypervisor or multipple hypervisors with common power source/network switch.

example: hyoervisors on same server rack
VMs on hypervisor with same power/networking = single fault domain

### Update domain
Groups of hypervisors (and VMs) that can be rebooted at same time

Planned hypervisor maintenance updates 
Not dependent on physical rack/location

Two VMs in same ipdate domain may be both be temporarily unavailable

### Spreading VMs across Update/Fault Domains
Adding static VMs to an availability set ensures VMs are placed:
- On hypervisors with separare maintenance windows
- On hypervisors on different server racks
=> High availability in case of power supply failure and/or rolling hypervisor updates

### Max limits
- 20 Updates Domains for your VM
- 3 Fault domain

### When to use availability sets
High Availability for multiple unique VMs that don't need auto-scaling

## Azure Virtual Desktop
### Definition
Provides virtualized windows desktops and apps hosted on Azure
- Virtual Desktop Interface (VDI) powered by Iaas (Vm) similar to Citrix
- Access from any device
- Separates OS, data and apps from local hardware
- Centrally managed and secure

### Problem to Solve
How to securely enable a remote Workforce ?

1. Data Security : secure data accessed from many locations
=> All data centrally stored in Azure includes desktop and apps

2. IT Overhead : manage multiple user desktops can be a nightmare
=> Apps, updates and settings centrally managed
=> Use existing Windows 10/11 licenses

3. Software consistency : making sure all users have consistent software and updates
=> Easily add more VMs to host pool
=> Multi-session environments

4. Scalability : Support growing workforce
=> Windows, Mac, mobile devices and web browser

### How it works
All resources are centrally hosted in Azure
Configuration, Access and Diagnostics
VM Host Pools

### Use cases
Remote Workforce enablement : Remote workspace environment from anywhere, no need for company hardware (BYOD: bring your own device friendly)

Secure Data Handling for healthcare : Secure, controlled access to sensitive patient data, reduced risk of data breaches, simplifies healthcare compliance

## App Services (Paas)
### Definition
Fully managed application hosting with minimal managemen overhead
Bring your code and Azure handles the rest.
No managing infrastructure.

### Things you don't have to manage
OS
Web server applications
Network management
High availability
Disk management
Load Balancers
Scaling

### Focus on What matters
Business Value and Your Code

### App Service hosting capabilities
Web Apps
- Support most languages
- Deploy static web apps
- Deploy containers
- No need to install/configure web server software
- Acccessible via Azure portal

WebJobs 
- Background tasks for application logic

API Apps
- Host your REST-based web API

Mobile Apps
- Backend for iOS/Android apps
- Authentication, mobile app data and push notifications

### Configuring and deploying app service (Web app)
Choose a unique name (must be unique across all of Azure)
Choose publish  (Code, container, static web app)
Choose a service plan (performance, scaling, disk space and more)
Deploy your code (Tight integration with github + other methods, support continuous deployment for rapid iteration)

## Azure Functions
### Definition
Serverless event-driven code execution

Extreme Paas : pratically zero management overhead
No VMs to manage
Apps only run when triggered

### What are Azure Functions
Sometimes referred to as functin as a service
![alt text](image-47.png)

### Architecture
Use VMs to work on
but no maintenance
nothing VM-related
Just focus on your functionality

### Use Case
Automated Image Resizing upon upload
Image uploaded to website => triggers an Azure Function Resize => Display on website

### Benefits
- Only runs when needed : event-driven (when an event triggers that function to run)
- Saves Money : no resources running means you don't pay for the function when it is not used
- Resilience : If your function fails, it doesn't affect other function instances
- Scalability : No configuration required, auto-scales based on demand, scales down to zero and up to your determined cap
- No infrastructure management : just deploy your code

## Introduction to Containers
### Definition
Lightweight, standalone package for apps
bundled application + dependencies : portable, self-contained unit, isolated from host OS

### Benefits
Manage Application Dependencies 
Less overhead
Increased portability
Efficiency
Consistency

### Containers vs VMs
Additional layer of virtualization:
- VMs: virtualized hardware
- Containers : virtualized OS : bild on top of host OS's kernel, can contain only services needed for application

### Container Workflow
Develop Application -> Application/Dependencies/execution/instructions packaged in a container -> Deploy container


## Container Deployment Options
### ACI : Azure Contaier Instances
- On-demand : use containerized applications to process data on demand, by only creating the container image when you need it
- Simplicity : minimum setup/overhead required, ideal for short-lived, simple workloads
- Not as scalable : single containers only, no load balancing/auto-scaling

### Azure Kubernetes Service (AKS)
Kubernetes : open-source container orchestration

- Orchestrate many containers : manage large scale, high volume, high complexity containerized workloads
more control and customization
- Scalability: automatic scaling, load balancing, and failover
- More complex + higher costs : persistent VMs nodes, between Iaas and Paas, much more complex than ACI

### Azure Container Apps
- In between ACI and AKS
- Serverless and scalable: ideal for serverless microservices, auto-scaling enabled
- Not quite as powerful as AKS : less customization

### Other deployment options
VMs : You can do anything with VMs, much more to install, manage, configure
Azure App service : ideal for long-running web applications, use any programming language
Azure Functions : Containerized event-driven applications, use any programming language
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
