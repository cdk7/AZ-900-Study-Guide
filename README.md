# Microsoft Azure Fundamentals (AZ-900) Complete Study Guide

This study guide prepares you for the **Microsoft Azure Fundamentals (AZ-900)** exam, an entry-level certification testing foundational knowledge of cloud concepts, Azure services, security, privacy, compliance, pricing, and support. No deep technical expertise is required—just a broad understanding of Azure fundamentals.

---

## Passed AZ-900 with 905!

## Table of Contents
1. [Cloud Computing Fundamentals](#1-cloud-computing-fundamentals)
   - [High Availability](#high-availability)
   - [Scalability and Elasticity](#scalability-and-elasticity)
   - [Fault Tolerance and Disaster Recovery](#fault-tolerance-and-disaster-recovery)
   - [Economic Benefits of Cloud Computing](#economic-benefits-of-cloud-computing)
   - [Shared Responsibility Model](#shared-responsibility-model)
   - [Cloud Service Models](#cloud-service-models)
2. [Cloud Deployment Models](#2-cloud-deployment-models)
   - [Public Cloud](#public-cloud)
   - [Private Cloud](#private-cloud)
   - [Hybrid Cloud](#hybrid-cloud)
3. [Core Azure Services](#3-core-azure-services)
   - [Azure Regions and Availability Zones](#azure-regions-and-availability-zones)
   - [Azure Resource Groups](#azure-resource-groups)
   - [Azure Compute Services](#azure-compute-services)
   - [Networking in Azure](#networking-in-azure)
   - [Storage in Azure](#storage-in-azure)
   - [Databases in Azure](#databases-in-azure)
   - [Azure Marketplace](#azure-marketplace)
4. [Security and Compliance](#4-security-and-compliance)
   - [Azure Security Tools](#azure-security-tools)
   - [Azure Compliance Offerings](#azure-compliance-offerings)
5. [Identity, Governance, Privacy, and Compliance](#5-identity-governance-privacy-and-compliance)
   - [Azure Active Directory (Azure AD)](#azure-active-directory-azure-ad)
   - [Role-Based Access Control (RBAC)](#role-based-access-control-rbac)
   - [Azure Policy](#azure-policy)
   - [Azure Blueprints](#azure-blueprints)
   - [Multi-Factor Authentication (MFA) & Conditional Access](#multi-factor-authentication-mfa--conditional-access)
   - [Microsoft Purview](#microsoft-purview)
6. [Core Solutions and Management Tools](#6-core-solutions-and-management-tools)
   - [Internet of Things (IoT) Solutions](#internet-of-things-iot-solutions)
   - [Big Data & Analytics](#big-data--analytics)
   - [Artificial Intelligence (AI)](#artificial-intelligence-ai)
   - [DevOps & Management Tools](#devops--management-tools)
7. [Azure Pricing, SLAs, and Service Lifecycles](#7-azure-pricing-slas-and-service-lifecycles)
   - [Azure Pricing Models](#azure-pricing-models)
   - [Azure Cost Management](#azure-cost-management)
   - [Service Level Agreements (SLAs)](#service-level-agreements-slas)
   - [Azure Support Plans](#azure-support-plans)
   - [Azure Free Trial and Subscriptions](#azure-free-trial-and-subscriptions)
   - [Service Lifecycle](#service-lifecycle)
8. [Exam Preparation Tips](#8-exam-preparation-tips)

---

## 1. Cloud Computing Fundamentals

### High Availability
- **Definition**: Systems operational and accessible most of the time, measured as uptime (e.g., 99.9%).
- **Factors Affecting Availability**:
  - Network outages
  - Application failures (e.g., bugs, misconfigurations)
  - System outages (e.g., VM crashes)
  - Power outages
  - Reliant system issues (e.g., database downtime)
- **Example**: A web app across multiple Azure regions with load balancing stays available if one region fails.

### Scalability and Elasticity
- **Scalability**: Adjust resources to meet demand.
  - **Scaling Out (Horizontal)**: Add more instances (e.g., extra VMs).
  - **Scaling Up (Vertical)**: Upgrade to stronger resources (e.g., 2-core to 8-core VM).
- **Elasticity**: Automatic scaling based on metrics (e.g., traffic spikes).
- **Example**: An e-commerce site scales out during sales, then scales back to save costs.

### Fault Tolerance and Disaster Recovery
- **Fault Tolerance**: System operates despite component failures.
- **Disaster Recovery**: Plans to recover from major outages (e.g., regional disasters).
- **Example**: Azure spreads VMs to avoid hardware failure impact; a BCDR plan replicates data to another region.

### Economic Benefits of Cloud Computing
- **CapEx vs. OpEx**:
  - **On-Premises (CapEx)**: Upfront hardware costs.
  - **Cloud (OpEx)**: Pay-as-you-go usage.
- **Economies of Scale**: Providers’ bulk purchasing lowers costs for users.
- **Example**: Using Azure VMs avoids idle on-premises servers, paying only for compute time.

### Shared Responsibility Model
- **Definition**: Divides duties between Microsoft and customers.
- **Examples**:
  - **IaaS**: Microsoft manages hardware; you manage OS and apps.
  - **PaaS**: Microsoft manages OS; you manage apps.
  - **SaaS**: Microsoft manages everything; you manage data.
- **Key Point**: Customer responsibility increases from SaaS to IaaS.

### Cloud Service Models
1. **Infrastructure as a Service (IaaS)**:
   - **Definition**: Virtualized resources; you manage OS/apps, provider handles hardware.
   - **Example**: Azure Virtual Machines (e.g., Windows Server VM).
   - **Benefits**: On-demand access, full control.
   - **Drawbacks**: You handle updates and management.
2. **Platform as a Service (PaaS)**:
   - **Definition**: Platform for app development; provider manages OS/infrastructure.
   - **Example**: Azure App Service for web apps.
   - **Benefits**: Simplified deployment, built-in tools (e.g., logging).
   - **Drawbacks**: Less flexibility, potential compatibility issues.
3. **Software as a Service (SaaS)**:
   - **Definition**: Fully managed software over the internet.
   - **Example**: Microsoft 365 (e.g., Office via browser).
   - **Benefits**: No maintenance, widely accessible.
   - **Drawbacks**: Limited customization, provider dependency.
4. **Serverless Computing**:
   - **Definition**: Code runs without managing servers; provider auto-scales.
   - **Example**: Azure Functions triggered by events (e.g., HTTP requests).
   - **Note**: Servers exist but are abstracted from the user.

---

## 2. Cloud Deployment Models

### Public Cloud
- **Definition**: Services over the public internet, open to all.
- **Characteristics**: Multi-tenant (shared resources).
- **Example**: Azure public cloud services.
- **Benefits**: Fast deployment, cost-effective.
- **Drawbacks**: Less control, security concerns.

### Private Cloud
- **Definition**: Dedicated cloud for one organization.
- **Characteristics**: Single-tenant (exclusive resources).
- **Example**: Government agency using dedicated Azure resources.
- **Benefits**: Enhanced security, compliance-friendly.
- **Drawbacks**: Higher cost if self-hosted.

### Hybrid Cloud
- **Definition**: Combines public and private clouds.
- **Example**: Azure App Service connecting to an on-premises database via Azure Arc.
- **Benefits**: Flexibility, legacy support.
- **Drawbacks**: Complex setup, compatibility challenges.

---

## 3. Core Azure Services

Azure provides a wide range of services to build, deploy, and manage applications. This section covers the foundational components—regions, resource groups, compute, networking, storage, databases, and the Azure Marketplace—explaining their roles and how they interact to create cohesive solutions.

### Azure Regions and Availability Zones
- **Definition**: 
  - **Regions**: Geographic locations containing one or more data centers, designed for low-latency and data residency (e.g., East US, West Europe). Azure has 60+ regions globally.
  - **Availability Zones**: Physically separate data centers within a region, each with independent power, cooling, and networking, ensuring high availability.
- **Detailed Explanation**: Regions allow you to deploy resources close to users or comply with data sovereignty laws (e.g., GDPR in Europe). Availability Zones add redundancy within a region, protecting against data center failures.
- **Examples**:
  - Deploying a web app in the East US region to serve US customers, using multiple Availability Zones to ensure uptime if one data center fails.
  - Hosting data in Germany North to meet German data residency requirements.
- **Relationships**: 
  - Regions and zones underpin all Azure services—compute, storage, and networking resources are deployed within them.
  - Compute services (e.g., VMs) can leverage zones for fault tolerance, while storage services (e.g., Blob Storage) can replicate across regions for disaster recovery.

### Azure Resource Groups
- **Definition**: Logical containers that group related Azure resources (e.g., VMs, databases, storage) for unified management, sharing the same lifecycle, permissions, and policies.
- **Detailed Explanation**: Resource groups simplify administration by allowing you to manage, monitor, and delete related resources together. They don’t dictate physical location—resources can span regions but belong to one group.
- **Examples**:
  - Grouping a web app’s VM, Azure SQL Database, and Blob Storage in a “WebApp-Prod” resource group for easy deployment and cost tracking.
  - Creating a “Test-Env” group for temporary resources, deleting it entirely when testing ends.
- **Relationships**:
  - Resource groups organize all other services (compute, networking, storage, databases) into manageable units.
  - They integrate with governance tools like Azure Policy and RBAC to enforce rules across grouped resources.

### Azure Compute Services
Azure offers various compute options to run applications, each suited to different workloads and management levels.

1. **Virtual Machines (VMs)**:
   - **Definition**: Emulated computers providing full control over the operating system (Windows/Linux) and applications.
   - **Detailed Explanation**: VMs are IaaS, giving you flexibility to install software, configure networks, and manage updates. They come in sizes (e.g., B-series for light workloads, D-series for general-purpose).
   - **Examples**:
     - Running a Windows Server VM with custom accounting software requiring specific configurations.
     - Deploying a Linux VM to host a legacy application migrated from on-premises.
   - **Relationships**: VMs often rely on Disk Storage for persistent data, VNets for networking, and Load Balancers for traffic distribution.

2. **Containers**:
   - **Definition**: Lightweight, portable environments for running applications consistently across platforms, managed via services like Azure Kubernetes Service (AKS).
   - **Detailed Explanation**: Containers package apps with dependencies, making them ideal for microservices. AKS automates orchestration, scaling, and updates for multiple containers.
   - **Examples**:
     - Using AKS to deploy a microservices-based e-commerce app (e.g., separate containers for payments, inventory).
     - Running a containerized Python app on Azure Container Instances (ACI) for quick testing.
   - **Relationships**: Containers can use Blob Storage for data, VNets for secure communication, and integrate with Azure Functions for event-driven tasks.

3. **App Services**:
   - **Definition**: A PaaS offering for hosting web apps, RESTful APIs, and mobile backends without managing underlying infrastructure.
   - **Detailed Explanation**: App Services abstracts server management, auto-scaling based on demand, and supports languages like .NET, Java, and Python. It includes built-in features (e.g., SSL, CI/CD).
   - **Examples**:
     - Deploying a .NET Core web app to serve a company website with auto-scaling during traffic spikes.
     - Hosting a REST API for a mobile app backend, connecting to Azure SQL Database.
   - **Relationships**: App Services often connect to Azure SQL or Cosmos DB for data, use VNets for secure access, and integrate with Azure AD for authentication.

4. **Azure Functions**:
   - **Definition**: Serverless compute service that runs code in response to events (e.g., HTTP requests, timers) without managing servers.
   - **Detailed Explanation**: Functions are ideal for lightweight, event-driven tasks, auto-scaling to zero when idle to save costs. You write code in languages like C#, Python, or JavaScript.
   - **Examples**:
     - Automatically resizing images uploaded to Blob Storage using an Azure Function.
     - Processing IoT sensor data from Azure IoT Hub every 5 minutes.
   - **Relationships**: Functions often trigger from Queue Storage messages, interact with Blob Storage or Cosmos DB, and use VNets for secure execution.

- **Compute Relationships**: 
  - VMs provide raw compute power and can host containers or App Services if configured manually.
  - Containers and App Services are higher-level abstractions, reducing management overhead compared to VMs.
  - Azure Functions complement all by handling specific tasks, often triggered by events from other compute or storage services.

### Networking in Azure
Networking services enable secure communication between Azure resources, the internet, and on-premises networks.

1. **Virtual Networks (VNet)**:
   - **Definition**: Private networks in Azure for secure resource communication, with subnets for isolation.
   - **Detailed Explanation**: VNets mimic on-premises networks, allowing IP address assignment and routing. They support peering (connecting VNets) and hybrid connectivity.
   - **Examples**:
     - Isolating a web server and database in separate subnets within a VNet for security.
     - Peering VNets in East US and West US for cross-region app communication.
   - **Relationships**: VNets host VMs, containers, and App Services, connecting them to Load Balancers, VPN Gateways, or Azure DNS.

2. **Load Balancers**:
   - **Definition**: Distributes incoming traffic across multiple servers to ensure availability and performance.
   - **Detailed Explanation**: Azure Load Balancer operates at Layer 4 (TCP/UDP), while Application Gateway (a related service) handles Layer 7 (HTTP/HTTPS) with advanced routing.
   - **Examples**:
     - Distributing user traffic across three web VMs to prevent overload.
     - Using Application Gateway to route traffic to different App Services based on URL paths.
   - **Relationships**: Load Balancers work with VMs or App Services in a VNet, often paired with Availability Zones for high availability.

3. **Azure DNS**:
   - **Definition**: Hosting and resolution service for DNS domains, translating names (e.g., www.example.com) to IP addresses.
   - **Detailed Explanation**: Azure DNS integrates with your resources, offering fast, reliable name resolution and custom domain management.
   - **Examples**:
     - Managing DNS records for “example.com” to point to an App Service.
     - Setting up a private DNS zone for internal VM communication within a VNet.
   - **Relationships**: Azure DNS links to VNets and public-facing services (e.g., App Services, Load Balancers) for name resolution.

4. **VPN Gateway**:
   - **Definition**: Securely connects on-premises networks to Azure VNets over the internet or private links (e.g., ExpressRoute).
   - **Detailed Explanation**: VPN Gateways enable hybrid scenarios, using IPsec for encryption. ExpressRoute offers dedicated, low-latency connections.
   - **Examples**:
     - Creating a site-to-site VPN between an office network and an Azure VNet.
     - Using ExpressRoute to connect a corporate data center to Azure for faster data transfer.
   - **Relationships**: VPN Gateways extend VNets to on-premises resources, often securing access to VMs or databases.

- **Networking Relationships**: 
  - VNets are the backbone, hosting compute resources and connecting them via Load Balancers or VPN Gateways.
  - Azure DNS resolves names for resources within VNets or publicly, enhancing accessibility.

### Storage in Azure
Azure storage services provide scalable, durable options for different data types.

1. **Blob Storage**:
   - **Definition**: Unstructured data storage for files (e.g., images, videos, backups) in tiers (Hot, Cool, Archive).
   - **Detailed Explanation**: Blob Storage is object-based, ideal for massive datasets, with tiers optimizing cost (e.g., Archive for rarely accessed data).
   - **Examples**:
     - Storing product images and videos for an e-commerce site.
     - Archiving old logs in the Archive tier for compliance.
   - **Relationships**: Blob Storage integrates with VMs (e.g., VM backups), App Services (e.g., static content), and Azure Functions (e.g., event triggers).

2. **File Storage**:
   - **Definition**: Managed file shares accessible via SMB protocol, replacing traditional file servers.
   - **Detailed Explanation**: File Storage supports hybrid access, syncing with on-premises servers via Azure File Sync.
   - **Examples**:
     - Migrating an on-premises file share to Azure Files for team access.
     - Mounting a file share to a VM for shared storage.
   - **Relationships**: File Storage mounts to VMs or containers within a VNet, complementing Blob Storage for structured file needs.

3. **Queue Storage**:
   - **Definition**: Message queues for asynchronous task processing between application components.
   - **Detailed Explanation**: Queues store millions of messages, enabling decoupled workflows (e.g., producer-consumer patterns).
   - **Examples**:
     - Queuing image processing tasks for an Azure Function.
     - Managing order processing between a web app and backend service.
   - **Relationships**: Queue Storage triggers Azure Functions and connects App Services or VMs in distributed apps.

4. **Disk Storage**:
   - **Definition**: Persistent, high-performance disks (e.g., SSD, HDD) for VM data.
   - **Detailed Explanation**: Disks attach to VMs, offering options like Premium SSD for speed or Standard HDD for cost savings.
   - **Examples**:
     - Attaching a Premium SSD to a VM running a database for low latency.
     - Using Standard HDD for a development VM with less critical data.
   - **Relationships**: Disk Storage is tied to VMs, providing OS and data persistence, often used with Blob Storage for backups.

- **Storage Relationships**: 
  - Blob Storage serves large-scale, unstructured needs, while File Storage offers traditional file shares.
  - Queue Storage enables async workflows with compute services, and Disk Storage supports VM operations.

### Databases in Azure
Azure provides managed database services for various data models and workloads.

1. **Azure SQL Database**:
   - **Definition**: Fully managed relational database based on Microsoft SQL Server.
   - **Detailed Explanation**: Offers features like auto-scaling, backups, and high availability (e.g., via geo-replication).
   - **Examples**:
     - Migrating an on-premises SQL Server CRM database to Azure SQL.
     - Running a web app’s backend with automatic failover to a secondary region.
   - **Relationships**: Azure SQL connects to App Services or VMs via VNets, often secured with Azure AD.

2. **Cosmos DB**:
   - **Definition**: Globally distributed, multi-model database (e.g., SQL, MongoDB) for low-latency access.
   - **Detailed Explanation**: Cosmos DB scales horizontally and replicates data across regions, ideal for real-time apps.
   - **Examples**:
     - Storing a global e-commerce catalog accessible worldwide.
     - Powering a gaming app with real-time leaderboards.
   - **Relationships**: Cosmos DB integrates with App Services, Azure Functions (e.g., event-driven updates), and Blob Storage (e.g., for media).

3. **Azure Database for MySQL/PostgreSQL**:
   - **Definition**: Managed open-source relational databases (MySQL, PostgreSQL).
   - **Detailed Explanation**: These services offer scalability, backups, and high availability for popular OSS databases.
   - **Examples**:
     - Hosting a WordPress site’s MySQL database in Azure.
     - Running a PostgreSQL analytics database for a BI tool.
   - **Relationships**: Links to App Services or VMs, often within VNets, and can sync with Blob Storage for backups.

- **Database Relationships**: 
  - Azure SQL and MySQL/PostgreSQL serve relational needs, while Cosmos DB handles global, non-relational workloads.
  - All connect to compute services (e.g., App Services, VMs) and use Blob Storage for backups or exports.

### Azure Marketplace
- **Definition**: A platform offering pre-built solutions and services from Microsoft and partners.
- **Detailed Explanation**: Marketplace provides templates (e.g., VM images, apps) to accelerate deployment, often integrating multiple Azure services.
- **Examples**:
  - Deploying a pre-configured Ubuntu VM with Nginx from the Marketplace.
  - Installing a third-party security tool (e.g., firewall) to protect a VNet.
- **Relationships**: Marketplace solutions often bundle compute (VMs, containers), storage, and networking, deployable into resource groups.

---

### Key Relationships Summary
- **Compute + Networking**: VMs, containers, and App Services run within VNets, using Load Balancers for traffic and VPN Gateways for hybrid connectivity.
- **Compute + Storage**: VMs use Disk Storage, App Services use Blob Storage for static files, and Azure Functions process Queue Storage messages.
- **Compute + Databases**: App Services and VMs connect to Azure SQL or Cosmos DB for data persistence.
- **Storage + Databases**: Blob Storage backs up databases; Queue Storage integrates with apps for async processing.
- **All Services + Regions/Zones**: Deployed within regions and zones for availability and compliance.
- **Resource Groups**: Unify all services for management, tying them to governance tools.
  
---

## 4. Security and Compliance

### Azure Security Tools
1. **Azure Security Center**:
   - **Definition**: Monitors and improves security posture.
   - **Example**: Identifying VM vulnerabilities.
2. **Azure Key Vault**:
   - **Definition**: Stores sensitive data (e.g., keys, passwords).
   - **Example**: Securing database connection strings.
3. **Azure Firewall**:
   - **Definition**: Network security for VNets.
   - **Features**: Stateful inspection, auto-scaling.
   - **Example**: Controlling outbound traffic.
4. **Azure DDoS Protection**:
   - **Definition**: Protects against DDoS attacks.
   - **Features**: Traffic monitoring, mitigation.
   - **Example**: Safeguarding gaming servers.
5. **Azure Sentinel**:
   - **Definition**: Cloud-native SIEM and SOAR solution.
   - **Features**: AI threat detection, automation.
   - **Example**: Monitoring suspicious logins.
6. **Azure Information Protection (AIP)**:
   - **Definition**: Classifies and protects sensitive data.
   - **Features**: Auto-labeling, persistent encryption.
   - **Example**: Encrypting patient records.
7. **Azure Advisor**:
   - **Definition**: Recommends improvements for cost, security, and performance.
   - **Example**: Suggesting MFA enablement.

### Azure Compliance Offerings
- **Definition**: Certifications and tools for regulatory compliance.
- **Key Offerings**:
  - ISO 27001/27002
  - GDPR
  - HIPAA/HITECH
  - SOC 1, 2, 3
  - PCI DSS
- **Example**: Proving GDPR compliance to regulators.

---

## 5. Identity, Governance, Privacy, and Compliance

### Azure Active Directory (Azure AD)
- **Definition**: Cloud-based identity and access management.
- **Example**: SSO across Microsoft 365 and Azure.

### Role-Based Access Control (RBAC)
- **Definition**: Fine-grained access control for Azure resources.
- **Example**: "Contributor" for devs, "Reader" for production.

### Azure Policy
- **Definition**: Enforces standards and assesses compliance.
- **Example**: Mandating storage encryption.

### Azure Blueprints
- **Definition**: Deploys pre-defined, compliant environments.
- **Example**: Setting up a compliant dept infrastructure.

### Multi-Factor Authentication (MFA) & Conditional Access
1. **MFA**:
   - **Definition**: Requires multiple verification methods.
   - **Example**: Password + mobile code for logins.
2. **Conditional Access**:
   - **Definition**: Controls access based on conditions.
   - **Features**: Location-based rules.
   - **Example**: MFA outside corporate networks.

### Microsoft Purview
- **Definition**: Data governance and compliance solution.
- **Example**: Tracking data lineage across Azure and on-premises.

---

## 6. Core Solutions and Management Tools

### Internet of Things (IoT) Solutions
1. **Azure IoT Hub**:
   - **Definition**: Connects IoT devices and apps.
   - **Example**: Collecting factory equipment data.
2. **Azure IoT Central**:
   - **Definition**: Managed IoT app platform.
   - **Example**: Managing smart building HVAC.
3. **Azure Sphere**:
   - **Definition**: Secure IoT device platform.
   - **Example**: Connecting consumer appliances.

### Big Data & Analytics
1. **Azure Synapse Analytics**:
   - **Definition**: Unified analytics for data warehousing.
   - **Example**: Analyzing retail sales trends.
2. **Azure Databricks**:
   - **Definition**: Spark-based analytics platform.
   - **Example**: Building ML models on large datasets.
3. **HDInsight**:
   - **Definition**: Open-source big data processing.
   - **Example**: Analyzing web logs with Hadoop.

### Artificial Intelligence (AI)
1. **Azure Machine Learning**:
   - **Definition**: Build and deploy ML models.
   - **Example**: Product recommendation system.
2. **Cognitive Services**:
   - **Definition**: APIs for vision, speech, and more.
   - **Example**: Speech-to-text in customer service.

### DevOps & Management Tools
1. **Azure DevOps**:
   - **Definition**: Tools for app lifecycle management.
   - **Example**: Automating app deployment.
2. **GitHub**:
   - **Definition**: Version control and collaboration.
   - **Example**: Source control with Azure integration.
3. **Azure Resource Manager (ARM) Templates**:
   - **Definition**: JSON files for infrastructure deployment.
   - **Example**: Deploying VMs and networking.
4. **Azure CLI & PowerShell**:
   - **Definition**: Command-line resource management.
   - **Example**: Automating Azure tasks.
5. **Azure Monitor**:
   - **Definition**: Monitors resource health and performance.
   - **Example**: Alerts for high VM CPU usage.

---

## 7. Azure Pricing, SLAs, and Service Lifecycles

### Azure Pricing Models
1. **Pay-As-You-Go**:
   - **Definition**: Pay based on usage, no upfront costs.
   - **Example**: Startup paying monthly for resources.
2. **Reserved Instances**:
   - **Definition**: Discounts for 1- or 3-year commitments.
   - **Example**: 40% savings on stable VM workloads.
3. **Spot Pricing**:
   - **Definition**: Discounts for unused capacity.
   - **Example**: 90% off for batch jobs on spot VMs.

### Azure Cost Management
- **Tools**:
  - **Pricing Calculator**: Estimates Azure costs.
  - **TCO Calculator**: Compares on-premises vs. Azure costs.
- **Example**: Using TCO to justify migration savings.

### Service Level Agreements (SLAs)
- **Definition**: Uptime guarantees with service credits for breaches.
- **Example**: VMs offer 99.9% (single) to 99.99% (zones); composite SLAs reflect lowest uptime in multi-service apps.

### Azure Support Plans
- **Definition**: Support tiers for Azure users.
- **Options**:
  - **Basic**: Free, no technical support.
  - **Developer**: Business hours support.
  - **Standard**: 24/7 support, <1-hour critical response.
  - **Professional Direct**: Proactive enterprise support.
- **Example**: Standard plan for production apps needing fast fixes.

### Azure Free Trial and Subscriptions
- **Options**:
  - **Free Account**: $200 credit, 12 months free services.
  - **Pay-As-You-Go**: Usage-based billing.
  - **Enterprise Agreements**: Volume licensing.
  - **Student Subscriptions**: Free services for students.
- **Example**: Students learning Azure with free credits.

### Service Lifecycle
1. **Preview Stage**:
   - **Definition**: Early access, no SLAs.
   - **Example**: Testing a new database service.
2. **General Availability (GA)**:
   - **Definition**: Fully supported production services.
   - **Example**: Migrating to a GA service.
3. **Deprecated Services**:
   - **Definition**: Phased-out services with migration guidance.
   - **Example**: Moving to a new authentication method.

---

## 8. Exam Preparation Tips
- Focus on **broad understanding**, not deep technical details.
- Learn **Azure portal navigation** and basic resource creation (e.g., VM, storage).
- Master **service models (IaaS, PaaS, SaaS)** and **deployment models (Public, Private, Hybrid)**.
- Study **security features** and the **shared responsibility model**.
- Understand **pricing factors**, **SLAs**, and **support options**.
- Use the **Azure free account** for hands-on practice.
- Review Microsoft’s [official AZ-900 exam objectives](https://learn.microsoft.com/en-us/certifications/exams/az-900).
- Take **practice tests** (e.g., MeasureUp, Whizlabs) to identify gaps.

---

Happy studying! Create a GitHub repository with this file (`AZ-900-Study-Guide.md`) to track your progress and share with others. Pair this guide with Microsoft Learn and practice exams for guaranteed success on AZ-900. Good luck!
