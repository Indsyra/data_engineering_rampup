# Course Overview

# Exam Overview

# Describing Cost Management in Azure

## Defining Cost Management in Azure
### What is cost management?
Set of financial tools available to anyone with access to a billing account, subscription, resource group or management group

The processes involved in planning evaluating and controlling the budget of a project or business

In Azure, it involves understanding and controlling where and how resources are being used and billed.

### Why cost management in Azure Matters ?
Unmonitored cloud expenses can lead to significant unplanned costs

Cost management ensures:
Predictable monthly bills
Efficient use of resources
Reduction of waste
Improved financial forecasting

### Azure Cost Management Tools
Azure CMB : Azure Cost Management and Billing allows viewing, analysing and optimising costs
Azure Advisor : personalised best practices to reduce costs
Azure Budgets : Set budgets and create alerts to monitor spending

## Subscriptions in Cost Management
### What are subscriptions ?
An agreement with Microsoft enabling access to its cloud services. Highest logical billing container

A boundary that delineates resource usage,access and billings

### How subscriptions relate to cost management

subscriptions = running tabs
every azure service consumed is billed to its associated subscription
at the end of the billing cycle, the "tab" is due.

### Azure Hierarchy Review
Management group have multiple subscription groups. Inside of a subscription, multiple resource groups. Inside a resource group, multiple resources.

###
### Subscription Offers
Pay-as-you-go: Pay for whqt is used without upfront costs
Enterprise Agreement - Commit to a certain level of usage in exchange for discounted rates
Azure Dev/Test - Discounted rates for development and testing environments, excluding production workloads
Free Account : Limited number of free services for a limited time and continuously

### Subscription Pricing Models

Reserved Instances
Spot pricing
Hybrid use benefits

## Factors that Influence Cost
Knowthe context of cost-saving measures
Commit whereit makes sense
Leverage the tool availablefor forecast

### Resource types
VMs billed based on comput,memory, storage, OS and time
Storage account - billed based on type (blob, file, disk, etc) and redundancy
Data transfers - inbound data is usually free, outbound costs
Databases - billed based on transactions and/or dedicated resources

### Location / Region
Azure is a global cloud offering
Consider deploying to lower cost regions but always consider latency and data residency

### Service Tiers
VMs (Basic vs Standard, Optimization (general purpose, memory, GPU), Std Hard Drive)
Storage accounts Blob (std vs prem), Files (prem, hot, cold), data lake, hdd vs SSD
Database : single vs elastic pool, vcore vs DTU, GP, BC, Hyper, Provisioned vs Serverless

Iier serction is a balance between cost and functionality requirement matters

### Reserved instances
commitment = savings
certain Azure services for a duration (1 or 3 years) in exchqnge of discounted rates, significant savings compared to pay-as-you-go pricing, requires upfront commitment,so assess your long-term needs carefully.

Predictable, steady-state workloads are prime candidates for Revervd instances

### Azure Hybrid benefit
Harness On-premises benefits



## Azure Pricing Calculator
###
###
###
###
###

## Using the Pricing Calculator
###
###
###
###
###

## Azure Total Cost of Ownership (TCO) Calculator
###
###
###
###
###

## Cost Management Tools
###
###
###
###
###

## Azure Budgets and Reservations
###
###
###
###
###

## Azure Cost Allocation and Recommendations
###
###
###
###
###

## Best Practices
###
###
###
###
###

## Exam Tips

# Features and tools for Governance and Compliance
## Defining Governance and Compliance
## Revisiting Azure Hierarchy
## Azure Policy
## Restricting Resource Access with Resource Locks
## Using Azure Policy and Resource Locks
## Publishing Governance and Compliance
## Microsoft Purview
## Securing Resources with Microsoft Defender for Cloud
## Understanding Governance Reports in Purview and Defender for Cloud
## Exam Tips

# Monitoring and Security Management Tools in Azure
## Monitoring and Management in Azure
## Azure Automation
## Azure Advisor
## Azure Monitor Overview
## Survey Resource Alerts Using Azure Monitor
## Log Analytics
## Azure Monitor Alerting
## Application Insights
## Azure Service Health
## Understanding Azure Monitor Alerting
## Expanding Management with Azure Arc
## Exam Tips