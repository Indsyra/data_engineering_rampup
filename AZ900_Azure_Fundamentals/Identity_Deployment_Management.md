# Exam overview

AZ900 starting point for a career in Azure. Entry-level Azure exam prove knowledge of cloud concepts and Azure services. For both IT experts and busines leaders

# Course overview

Identity, Deployment And Management : what each of these means and how they are accomplished in Azure, describe the tools used for each concept, launching point for pursuing specific areas of Azure

# Defining Identity Authentication and Authorization

## Scope Definitions
Identity : who or what I am
unique identifier for any digital object

Authentication : the proof of who/what I am
proves identity

Authorization : where I can go and what I can do
scoped identity

## Examples

### Identity
Physical world : passport, driver's license, hospital ID
Digital world : Azure Active Directory (AD) object, software license, email ID

### Authentication
Physical world : house key, certificate or authenticity, safety deposity box password
Digital world : SSH key, SSL certificate, Email account password

### Authorization
Physical world : Event ticket, Gate-specific key code, Key card
Digital world : Application secret, Shared access signature token, Key card

## Management

All the resources and services available in Microsoft's cloud offering

Azure AD : service for managing identity, authentication and authorization => Microsoft Entra ID

# Azure Active Directory

## Microsoft Entra
New product family
AD is a key component of Entra
Other components are : Permissions management and Verified ID
Exam perspective : Know that Azure AD is part of the broader Microsoft Entra product family

## Directory Services
Azure Active Directory Domain Services
Azure Active Directory (now Microsof Entra ID)

## Azure AD vs AD

Az AD : Modern office solution and designed for modern web, using modern authentication
Modern architecture, protocols and methods
Cloud native design

AD: Legacy office solution designed for legacy web and using legacy authentication
Legacy architecture, protocols and methods
On-premises/datacenter design

AZ active directory domain services : managed service for an AD to use modern 

## Entra ID
Active Directory is not Microsoft Entra ID

## Characteristics
Requirements :
- Every azure account automatically has an Azure AD instance with it
- Every Azure AD instance needs at least one user and this user is created with the initial Azure AD instance
- Custom domain name
- Azure AD Connect (if on-premises AD present)

## Organization
Tenant : represents the organization. It is dedicated instance of Azure AD that an organization receives when signing up for Azure. Each tenant is distinct and completely separate from other Azure AD tenants, Max 500 Tenants : each user in Azure can be a member or guest of up to 500 Azure AD/Microsoft Entra ID tenants

Subscription: All resources within a subscription are billed together, you can have multiple subscriptions within a tenant to separate costs + if a subscripion isn't paid, all the reources and services associated with the subscription stop. => a billing entity

On-Prmises => Azure AD => Azure
Azure AD/ENtra ID can help manage users in a hybrid organization

## Create a group and add a member in Microsoft Entra ID
EID : Entra ID

Search Microsoft Entra ID
Click on Groups then on display all groups
Fill the blanks (Name and description) by leaving Group type as Security
Click on Users
Create new User
Go to groups add members or owners

## Zero trust concepts
classic trusted vs untrusted model are not well suited for many modern 
pusheds trust to the individual level

- Trusted perimeter
Trust boundary for secure access
Example : Corporate Network
Must be on corporate network to access resources
Use VPN as an extension of trusted perimeter

Zero trust : all users assumed untrustworthy unless proven otherwise (trusted by identity, regardless of location, least privilege access, simplified, centralized management)
In action : Access Microsoft 365 email, documents and resources for remote workforce, centrally control access with conditional access policies (access from anywhere, authenticate with identity), allow access only from approved managed deices (independent from network location)

## Multi-factor authentication

MFA Model : Something you know, sthg you have, sthg you are
=> MFA Example : validate what you know (username/password), validate what you have (phone validation)
MFA provides layered security for user identity
requires at least two components of sthg you know/have/are

## Conditional access
feature that provides additional layer of security to your environments and identity
its rules are essentially if/then statements that permit or deny access depending on whether the rules are met.
MFA is often implemented with conditional access as further security.

Authentication protections beyond username/password

if/then policy to grant access : if user meets these conditions
often paired with MFA

Create conditional access policy : assign signals (conditions : users/groups, application to grant/deny access, location, approved devices), access decisions (grant/block access, require MFA)

Scenarios : Enforce MFA for all administrators/users, block sign-ins using legacy authentication protocols, grant access only to specific locations, require organisation-manage devices for application sign-in