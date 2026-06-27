# my-project-azure
assignment

MDCopyAzure Free Tier Account Setup — Complete Documentation

ProLaunch Careers × Afriment | Cohort 19 | Team HACK
Cloud Computing Track | Azure Free Tier Assignment


Table of Contents


Project Overview
Account Creation Documentation
Azure Portal Navigation
Dashboard Customization
Governance Setup — Subscription & Resource Group
Identity & Access Management (IAM/RBAC)
Region Selection
Resource Deployment (Test)
Billing and Cost Management
Free Tier Limits and Summary
Security Considerations & MFA Setup
Completion Checklist & Troubleshooting



1. Project Overview

Description

This project documents the practical setup of a Microsoft Azure cloud environment using the Azure Free Tier. It serves as a hands-on demonstration of foundational cloud computing skills, covering account registration, portal navigation, governance configuration, identity management, resource deployment, cost monitoring, and security best practices.

Project Goals


Establish a functional cloud environment using the Azure Free Tier
Gain proficiency in navigating the Azure Portal and understanding its organizational structure
Understand cloud governance fundamentals, including subscriptions and resource groups
Learn basic Identity and Access Management (IAM) concepts such as Role-Based Access Control (RBAC)
Develop an awareness of cloud cost management, regions, and the shared responsibility security model
Understand the differences between IaaS, PaaS, and SaaS service models within a real-world platform


Repository Structure

azure-free-tier-setup/
├── README.md                        ← This file
├── screenshots/
│   ├── 01_account_creation/
│   │   ├── signup_form.png
│   │   ├── email_verification.png
│   │   ├── phone_verification.png
│   │   ├── credit_card_entry.png
│   │   └── account_created_success.png
│   ├── 02_portal_navigation/
│   │   ├── portal_home.png
│   │   ├── services_menu.png
│   │   └── search_function.png
│   ├── 03_dashboard/
│   │   └── customized_dashboard.png
│   ├── 04_governance/
│   │   ├── subscription_overview.png
│   │   └── resource_group_created.png
│   ├── 05_iam/
│   │   └── entra_id_overview.png
│   ├── 06_billing/
│   │   ├── cost_management_home.png
│   │   └── budget_alert_75pct.png
│   ├── 07_security/
│   │   └── mfa_setup.png
│   └── 08_resource_deployment/
│       └── vm_or_storage_created.png
└── docs/
    └── azure-free-tier-setup.docx   ← Full Word document version


2. Account Creation Documentation

Step-by-Step Process

Follow these steps carefully to create your Azure Free Tier account:

Step 1 — Navigate to the Sign-Up Page


Open a browser and go to: https://azure.microsoft.com/free
Click "Start free"



Screenshot required: Landing page with "Start free" button visible



Step 2 — Sign In or Create a Microsoft Account


Click "Create one" if you do not have a Microsoft account
Enter your preferred email address (personal or work email)
Create a strong password
Click "Next"



Screenshot required: Sign-up form with email field filled in



Step 3 — Email Verification


Microsoft will send a verification code to the email you provided
Open your inbox, copy the 6-digit code
Enter the code in the verification field on screen
Click "Verify"



Screenshot required: Email verification screen with code input field



Step 4 — Phone Number Verification


Select your country code (e.g., +234 for Nigeria)
Enter your mobile phone number
Click "Send code" (SMS) or "Call me"
Enter the received verification code
Click "Verify"



Screenshot required: Phone verification screen



Step 5 — Credit/Debit Card Entry


Enter your valid credit or debit card details
This is required for identity verification — you will not be charged during the free tier period
Azure provides $200 USD free credit for 30 days
Click "Next" after entering card details



Screenshot required: Payment information form (card number masked for security)



Step 6 — Agreement and Account Activation


Review the subscription agreement and privacy statement
Check the box to agree to the terms
Click "Sign up"
Wait for the account to be created (this may take 1–2 minutes)



Screenshot required: Successful account creation confirmation screen



Step 7 — Access the Azure Portal


Click "Go to Azure portal" or navigate to https://portal.azure.com
Sign in with your newly created credentials



Screenshot required: Azure Portal home screen after first login




3. Azure Portal Navigation

The Azure Portal is a unified web-based console for managing all Azure services and resources.

Key Navigation Areas

AreaLocationPurposeHomeportal.azure.comDefault landing page with quick access tilesSearch BarTop centerSearch for services, resources, or documentationPortal MenuTop-left hamburger iconExpand/collapse the global navigation sidebarAzure ServicesHome page gridQuick links to Compute, Storage, Networking, Databases, etc.Notifications BellTop-rightView deployment and activity alertsSettings GearTop-rightPortal appearance, language, and layout preferencesProfile IconTop-rightAccount info, sign out, switch directory

Primary Service Categories (Navigation Menu)


Compute — Virtual Machines, App Services, Functions
Storage — Blob Storage, File Shares, Queues
Networking — Virtual Networks, Load Balancers, DNS
Databases — Azure SQL, Cosmos DB, Database for MySQL
Security — Microsoft Defender for Cloud, Key Vault


Breadcrumb Navigation

Azure uses breadcrumb trails at the top of each blade (panel), e.g.:

Home > Resource groups > MyResourceGroup > myVirtualMachine

This allows you to navigate back to any parent level without using the browser back button.

Search Functionality


Use the top search bar to find any Azure service by name
Results are grouped into: Services, Resources, Marketplace, and Documentation
Example search: type "Virtual Machine" to jump directly to the VM creation page



Screenshot required: Portal home page with navigation menu and search bar visible




4. Dashboard Customization

The Azure Dashboard is a customizable page that provides an at-a-glance view of your cloud environment.

Steps to Customize the Dashboard


From the Azure Portal home, click "Dashboard" in the left sidebar (or click the Dashboard icon)
Click "Edit" at the top of the dashboard
From the Tile Gallery on the left, drag and drop tiles onto the canvas:

All resources — shows all deployed resources
Service health — displays Azure platform status
Cost Management — shows current spend vs. budget
Resource groups — quick link to your resource containers
Quickstart tutorials — links to learning content



Resize tiles by dragging their corners
Rearrange tiles by dragging them to new positions
Click "Save" when done


Recommended Tile Configuration

TilePurposeAll ResourcesMonitor everything you've deployedCost ManagementStay within free tier limitsResource GroupsNavigate to your project containersService HealthCheck for Azure outages in your regionAzure Active DirectoryQuick access to identity settings


Screenshot required: Customized dashboard with at least 4 tiles configured




5. Governance Setup — Subscription & Resource Group

Identifying Your Subscription


In the Azure Portal, search for "Subscriptions" in the top search bar
Click on Subscriptions from the results
You will see your "Azure subscription 1" (Free Trial) listed
Click on it to view:

Subscription ID (a unique GUID)
Offer type: Free Trial or Pay-As-You-Go
Status: Active
Billing cycle and period






Screenshot required: Subscriptions overview page showing your active subscription



Creating a Resource Group

A Resource Group is a logical container that holds related Azure resources. Think of it like a project folder.

Steps:


In the search bar, type "Resource groups" and select it
Click "+ Create"
Fill in the following:

Subscription: Azure subscription 1 (Free Trial)
Resource group name: e.g., ProLaunch-CloudProject-RG
Region: Choose a region close to your location (e.g., South Africa North or West Europe)



Click "Review + create"
Click "Create" to confirm



Screenshot required: Resource group successfully created, showing in the Resource Groups list



Why Resource Groups Matter


They allow you to manage, deploy, and delete resources together as a unit
You can assign access permissions (RBAC) at the resource group level
Useful for organizing resources by project, environment (dev/test/prod), or team



6. Identity & Access Management (IAM/RBAC)

Azure Active Directory / Microsoft Entra ID


Search for "Microsoft Entra ID" (formerly Azure Active Directory) in the portal
This opens the identity management panel for your tenant
Key sections to explore:

Overview — Tenant ID, user count, domain
Users — View and manage user accounts
Groups — Organize users for bulk permission assignment
App registrations — Register applications for API access
Roles and administrators — View built-in role definitions






Screenshot required: Microsoft Entra ID overview page showing tenant details



Role-Based Access Control (RBAC)

RBAC controls who can do what on which Azure resources.

RolePermissionsOwnerFull access including ability to manage access for othersContributorCan create and manage resources, cannot grant accessReaderRead-only access to resourcesUser Access AdministratorCan manage user access to resources

Viewing Role Assignments on a Resource Group:


Go to your Resource Group (ProLaunch-CloudProject-RG)
In the left menu, click "Access control (IAM)"
Click "Role assignments" tab
Here you can see who has what role on this resource group
To add: click "+ Add" → "Add role assignment"



7. Region Selection

What is a Region?

An Azure region is a geographic area containing one or more data centers. Choosing the right region affects:


Latency (speed of response to your users)
Data residency (legal/compliance requirements)
Service availability (not all services are in every region)
Cost (pricing can vary by region)


Recommended Regions for Nigeria-Based Users

RegionApproximate LatencyNotesSouth Africa North (Johannesburg)~50–80msClosest Azure region to NigeriaWest Europe (Netherlands)~80–120msGood alternative with broad service coverageUK South (London)~80–110msWell-connected to West Africa

How to Check Latency


Visit https://www.azurespeed.com
This tool pings Azure data centers from your location and displays latency per region
Choose the region with the lowest latency for best performance


Availability Zones

Within a region, Azure has Availability Zones — physically separate data centers designed for high availability. For the free tier, zone-redundant deployment is not required but is good to understand.


8. Resource Deployment (Test)

This section documents a test deployment of a basic Azure resource to validate the account and understand the provisioning workflow.

Option A: Create a Virtual Machine (IaaS)


Search for "Virtual machines" and click "+ Create" → "Azure virtual machine"
Configure the basics:

Subscription: Azure subscription 1
Resource group: ProLaunch-CloudProject-RG
Virtual machine name: ProLaunch-TestVM
Region: South Africa North
Image: Ubuntu Server 22.04 LTS (free tier eligible)
Size: Standard_B1s (1 vCPU, 1 GB RAM) — free tier eligible
Authentication: SSH public key or Password



Click "Review + create" → "Create"
Wait for deployment to complete (2–3 minutes)
Verify the VM appears in "All resources"



IMPORTANT: Stop or delete the VM after testing to avoid consuming your free credits.



Option B: Create a Storage Account (Alternative)


Search for "Storage accounts" → click "+ Create"
Configure:

Resource group: ProLaunch-CloudProject-RG
Storage account name: prolauncstorage01 (must be globally unique)
Region: South Africa North
Performance: Standard
Redundancy: LRS (Locally Redundant Storage)



Click "Review + create" → "Create"



Screenshot required: Deployed resource showing in "All resources" or Resource Group




9. Billing and Cost Management

Accessing the Billing Dashboard


Search for "Cost Management + Billing" in the portal
Under Billing, click "Billing accounts" to view your free tier account
Under Cost Management, click "Cost analysis" to see spending breakdown


Free Tier Benefits

BenefitDetailsFree credit$200 USD valid for 30 daysAlways-free services12 months of popular services at limited quantitiesPermanent free tier55+ services always free (e.g., Azure Functions — 1M requests/month)

Setting Up a Budget Alert at 75%

This is a required rubric item. Follow these steps:


Go to Cost Management + Billing → Cost Management → Budgets
Click "+ Add"
Configure the budget:

Name: FreeTierBudget
Reset period: Monthly
Budget amount: $200 (or your credit amount)



Click "Next: Alerts"
Under Alert conditions:

Type: Actual
% of budget: 75
Email recipients: Enter your email address



Click "Create"



Screenshot required: Budget configuration screen showing 75% alert threshold set and saved



Navigating Cost Management


Cost analysis: Break down spending by service, resource group, or time period
Budgets: Set spending limits with email/SMS alerts
Advisor recommendations: Cost optimization suggestions from Azure
Invoices: View billing history (will be empty on free tier if no overages)



10. Free Tier Limits and Summary

Free Trial (First 30 Days)


$200 USD credit usable on any Azure service
Credit expires after 30 days even if unused
Expiry date: 12 months from account creation (for 12-month free services)


12-Month Free Services (Selected)

ServiceFree LimitVirtual Machines (B1s Linux)750 hours/monthVirtual Machines (B1s Windows)750 hours/monthManaged Disks64 GB × 2 (P6)Blob Storage5 GB LRS hotAzure SQL Database250 GBAzure Cosmos DB25 GB + 1,000 RU/sBandwidth (outbound)15 GB/month

Always-Free Services (Permanent)

ServiceFree LimitAzure Functions1,000,000 requests/monthAzure App Service10 web/mobile/API appsAzure DevOps5 usersAzure Active Directory50,000 objectsAzure Kubernetes ServiceFree cluster management

Resource Quotas


vCPU quota (free tier): 4 vCPUs per region
Public IP addresses: 10 (basic)
Storage accounts: 250 per subscription



⚠️ Warning: Exceeding free tier limits or using non-free-tier services will charge your credit card. Always monitor Cost Management.




11. Security Considerations & MFA Setup

Account Security Settings


Go to your Microsoft Account at https://account.microsoft.com
Navigate to Security → Advanced security options


Enabling Multi-Factor Authentication (MFA)

MFA adds a second layer of security beyond your password. This is strongly recommended.

Steps to Enable MFA:


In the Azure Portal, go to Microsoft Entra ID → Users → click your user account
At the top, click "Per-user MFA" or navigate to the MFA settings
Click "Enable" for your account
On next login, you will be prompted to set up MFA using:

Microsoft Authenticator app (recommended)
SMS text message
Phone call





Setting Up Microsoft Authenticator (Recommended):


Download the Microsoft Authenticator app on your mobile phone
In the MFA setup screen, scan the QR code with the app
Enter the 6-digit code shown in the app to verify
Save your backup codes in a secure location



Screenshot required: MFA successfully enabled on your account (showing "Enabled" status)



Password Policy Best Practices

RecommendationDetailMinimum length12+ charactersComplexityMix uppercase, lowercase, numbers, and symbolsNo reuseDo not reuse the last 5 passwordsChange frequencyEvery 90 days for sensitive accounts

Trusted Devices


In Microsoft Entra ID → Security → Conditional Access (view only on free tier)
Trusted devices reduce repeated MFA prompts on personal/work machines


Azure Security Best Practices (Shared Responsibility Model)

Azure ManagesYou ManagePhysical data center securityIdentity and access (IAM)Network infrastructureOperating system patching (VMs)Hardware failuresApplication securityPlatform availabilityData encryption at rest/transit


12. Completion Checklist & Troubleshooting

Verification Checklist

Use this checklist to confirm all tasks have been completed:


 Account Creation — Microsoft Azure account created successfully with email verified
 Phone Verification — Mobile number verified during signup
 Payment Method — Credit/debit card added (no charge on free tier)
 Portal Access — Successfully logged into portal.azure.com
 Portal Navigation — Explored main navigation, services menu, search function
 Dashboard Customization — Custom dashboard created with 4+ tiles
 Subscription Identified — Free Trial subscription located and reviewed
 Resource Group Created — New resource group ProLaunch-CloudProject-RG created
 Entra ID Explored — Microsoft Entra ID (Azure AD) overview reviewed
 RBAC Reviewed — Role assignments understood and reviewed on resource group
 Region Selected — Optimal region identified using latency tool
 Resource Deployed — Test VM or Storage Account created successfully
 Budget Alert Set — Budget alert configured at 75% of free credit
 Free Tier Limits Reviewed — 12-month and always-free services documented
 MFA Enabled — Multi-Factor Authentication enabled on account
 Security Settings Reviewed — Password policy and trusted devices configured
 Screenshots Captured — All required screenshots added to the screenshots/ folder
 README Completed — This file is complete and committed to the GitHub repository
 Repository Made Public — GitHub repository set to Public visibility


Troubleshooting Guide

Issue: "Sign-up is not available in your region"

Solution: Use a VPN temporarily during sign-up, or try the Azure for Students offer which has fewer geographic restrictions.

Issue: Credit card not accepted

Solution: Try a Visa or Mastercard debit card with online transactions enabled. Some prepaid cards are not accepted. Contact your bank to enable international online transactions.

Issue: "You have no subscriptions"

Solution: This can occur if the free trial activation did not complete. Go to https://azure.microsoft.com/free and sign in again to re-activate.

Issue: Free tier expired or credits used up

Solution: Go to Cost Management + Billing → check if you have been upgraded to Pay-As-You-Go. You can set a spending limit under Billing → Spending limit to prevent charges.

Issue: VM deployment fails with "quota exceeded"

Solution: Free tier accounts have a vCPU quota limit (typically 4 per region). Try a different region or choose a smaller VM size (B1ls).

Issue: Cannot find a service in the portal

Solution: Use the top search bar — it searches all Azure services, resources, and documentation simultaneously.


Support Resources

ResourceLinkAzure Free Account FAQhttps://azure.microsoft.com/free/free-account-faqAzure Documentationhttps://docs.microsoft.com/azureAzure Cost Management Docshttps://docs.microsoft.com/azure/cost-management-billingMicrosoft Learn (Free Training)https://learn.microsoft.comAzure Status Pagehttps://status.azure.comAzure Community Forumhttps://techcommunity.microsoft.com/azure


Next Steps

After completing this assignment, consider exploring:


Azure Functions — Build serverless event-driven applications (always free tier)
Azure App Service — Deploy web applications without managing infrastructure
Azure DevOps — Set up CI/CD pipelines for your code
Azure Monitor — Set up logging, metrics, and alerts for your resources
ARM Templates / Bicep — Learn infrastructure-as-code for Azure



Documentation prepared by: Esther Jonathan
Programme: ProLaunch Careers × Afriment | Cohort 19 | Team HACK
Track: Cloud Computing
Date: June 2026
