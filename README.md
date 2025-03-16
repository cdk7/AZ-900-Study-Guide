# Microsoft Azure Fundamentals (AZ-900) Complete Study Guide

This study guide prepares you for the **Microsoft Azure Fundamentals (AZ-900)** exam, an entry-level certification testing foundational knowledge of cloud concepts, Azure services, security, privacy, compliance, pricing, and support. No deep technical expertise is required—just a broad understanding of Azure fundamentals.

---

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

### Azure Regions and Availability Zones
- **Regions**: Geographic areas with multiple data centers (60+ worldwide).
- **Availability Zones**: Isolated data centers within a region with independent power, cooling, and networking.
- **Example**: Deploying apps across East US zones for high availability.

### Azure Resource Groups
- **Definition**: Logical containers for managing related Azure resources.
- **Example**: Grouping VMs, databases, and storage for a web app.

### Azure Compute Services
1. **Virtual Machines (VMs)**:
   - **Definition**: Emulated computers with full OS control.
   - **Example**: Windows/Linux VMs for custom apps.
2. **Containers**:
   - **Definition**: Lightweight, portable app environments.
   - **Example**: Azure Kubernetes Service (AKS) for microservices.
3. **App Services**:
   - **Definition**: PaaS for hosting web apps/APIs.
   - **Example**: Deploying a .NET app to Azure App Service.
4. **Azure Functions**:
   - **Definition**: Serverless compute for event-driven code.
   - **Example**: Resizing images in blob storage.

### Networking in Azure
1. **Virtual Networks (VNet)**:
   - **Definition**: Secure communication for Azure and on-premises resources.
   - **Example**: Isolating web and database servers in subnets.
2. **Load Balancers**:
   - **Definition**: Distributes traffic across servers.
   - **Example**: Balancing traffic across web VMs.
3. **Azure DNS**:
   - **Definition**: DNS hosting and resolution.
   - **Example**: Managing company domain DNS in Azure.
4. **VPN Gateway**:
   - **Definition**: Secure on-premises-to-Azure connections.
   - **Example**: Site-to-site VPN for office-to-Azure links.

### Storage in Azure
1. **Blob Storage**:
   - **Definition**: Unstructured data storage (e.g., images, videos).
   - **Example**: Storing e-commerce product media.
2. **File Storage**:
   - **Definition**: Managed SMB file shares.
   - **Example**: Migrating on-premises shares to Azure Files.
3. **Queue Storage**:
   - **Definition**: Message storage for async tasks.
   - **Example**: Managing tasks in a distributed app.
4. **Disk Storage**:
   - **Definition**: High-performance VM disk storage.
   - **Example**: Premium SSDs for database VMs.

### Databases in Azure
1. **Azure SQL Database**:
   - **Definition**: Managed SQL Server database.
   - **Example**: Migrating on-premises SQL databases.
2. **Cosmos DB**:
   - **Definition**: Globally distributed, multi-model database.
   - **Example**: Storing a global product catalog.
3. **Azure Database for MySQL/PostgreSQL**:
   - **Definition**: Managed MySQL/PostgreSQL services.
   - **Example**: Hosting a WordPress MySQL database.

### Azure Marketplace
- **Definition**: Platform for pre-built solutions from Microsoft and partners.
- **Example**: Deploying a third-party firewall VM.

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
