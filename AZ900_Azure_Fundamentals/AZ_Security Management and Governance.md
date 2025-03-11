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
Leverage the tool available to forecast what cost might be

### Resource types
VMs billed based on comput,memory, storage, OS and time
Storage account - billed based on type (blob, file, disk, etc) and redundancy (local, regional, global)
Data transfers - inbound data is usually free, outbound costs
Databases - billed based on transactions and/or dedicated resources (depends on the type of the type of database)

### Location / Region
Azure is a global cloud offering
Variation can be influenced by: local regulations, energy costs and demand within the region or data centers
Consider deploying to lower cost regions but always consider latency and data residency

### Service Tiers
VMs (Basic vs Standard, Optimization (general purpose, memory, GPU), Std Hard Drive)
Storage accounts Blob (std vs prem), Files (prem, hot, cold), data lake (std vs prem), hdd vs SSD (std, prem, ultra)
Database : single vs elastic pool, vcore vs DTU, GP (general purpose), BC (business critical), Hyper, Provisioned vs Serverless

Tier selection is a balance between cost and functionality requirement matters
Know your requirement first to know how to navigate

### Reserved instances
commitment = savings
certain Azure services for a duration (1 or 3 years) in exchqnge of discounted rates, significant savings compared to pay-as-you-go pricing, requires upfront commitment,so assess your long-term needs carefully.
Significant savings compared to pay-as-you-go pricing
Requires upfront commitment, so assess your long-term needs carefully
Predictable, steady-state workloads are prime candidates for Revervd instances

### Azure Hybrid benefit
Harness On-premises benefits exploiter les avantages sur site
leveraging on-prem licenses
different support tiers come at different costs
add-ons, extensions or third-party services



## Azure Pricing Calculator

### Forecasting your cloud expenditures

### Your first step to cost prediction
Product tools
Product categories
Product Picker

### Building your azure financial plan
Consider the type and scale of your deployment requirements and input them into the calculator
Experiment with flexible requirements (tiers, instance types)
Be aware of your hard requirements (regions, data transfer needs)

### Deciphering the calculator's output
Cost breakdown : Visualization, Time period (daily, monthly, yearly)
Monthly Cost Estimate : Fixed vs Variable, peak costs, reservations, discount
Other costs : Data transfer, Bundled pricing, Licensing, Support, Add-ons

### Refining your financial forecast
Export results to formats that can be integrated into financial tools and/or shared
Adjust various parameters to discover cost-saving (scaling, regions, instances, etc)
Use the estimate in larger cost management strategy
Set budget, monitor costs and continually optimize

Azure advisor for recommendations

### Common mistakes
- Overestimatin resource needs : start small and scale up if needed
- Forgetting data transfer costs
- Ignoring price variations by region
- Not factoring in (or assuming) discounts

### Tips for more accurate estimates
- Regularly update usage patterns
- Factor in growth
- Use Azure's pricing examples
- Stay up to date with pricing changes

## Using the Pricing Calculator

Great for estimating what your cloud cost could look like
excellent way to explore the question "what if I deployed a"
should not be taken as a quote for costs

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