# AZ-900 Domain 1: Cloud Concepts

## 1. The Shared Responsibility Model
Who manages what across infrastructure layers:

| Layer | On-Premises | IaaS | PaaS | SaaS |
| :--- | :--- | :--- | :--- | :--- |
| **Data & Access (Identity)** | Customer | Customer | Customer | Customer |
| **Client Devices & Network** | Customer | Customer | Customer | Customer |
| **Applications** | Customer | Customer | Customer | Microsoft |
| **OS & Runtime** | Customer | Customer | Microsoft | Microsoft |
| **Virtualization & Compute** | Customer | Microsoft | Microsoft | Microsoft |
| **Physical Hosts, Network, Datacenter** | Customer | Microsoft | Microsoft | Microsoft |

> **Exam Rule:** In **all** cloud models, the **Customer** is always responsible for **Data**, **Endpoints**, and **Account/Identity Access Management**.

---

## 2. Cloud Service Models Mapped to Your Active Projects

- **IaaS (Infrastructure as a Service):** 
  - Azure Virtual Machines, Azure VNet, Azure Storage disks.
  - *Context:* Renting an Ubuntu Linux VM in Azure and manually installing Node.js, Git, and running `pnpm dev`. You patch the OS.
- **PaaS (Platform as a Service):** 
  - Azure Static Web Apps, Azure App Service, Azure SQL Database.
  - *Context:* Linking your GitHub repo directly to Azure Static Web Apps. Azure handles the Node runtime, OS patching, and SSL certificates automatically.
- **SaaS (Software as a Service):** 
  - Microsoft 365, GitHub, Power Platform.
  - *Context:* Using GitHub or Outlook web portal. Zero infrastructure, runtime, or codebase configuration needed.

---

## 3. Financial Models: CapEx vs. OpEx

- **CapEx (Capital Expenditure):** 
  - Upfront, one-time spending on physical hardware (e.g., buying a server rack, routers, cooling).
  - High initial investment, value depreciates over years, inflexible.
- **OpEx (Operational Expenditure):** 
  - Ongoing, operational spending on consumption (e.g., paying monthly cloud bills).
  - No upfront hardware costs, pay-as-you-go, scalable.
- **Consumption-based Pricing:** Cloud computing uses OpEx; you pay only for the compute cycles, memory, and bandwidth consumed.

---

## 4. Architectural Cloud Advantages

- **High Availability (HA):** Ensuring systems stay operational with near-zero downtime (guaranteed by SLAs).
- **Scalability:**
  - *Vertical Scaling (Scale Up):* Adding more CPU/RAM to an existing virtual machine.
  - *Horizontal Scaling (Scale Out):* Adding more VM instances to handle traffic spikes.
- **Elasticity:** The system's automated ability to scale resources up *and* down dynamically based on live demand.
- **Agility:** The ability to provision, test, and deploy cloud resources in minutes rather than weeks.
- **Geo-Distribution:** Deploying apps closer to regional users to reduce network latency.
