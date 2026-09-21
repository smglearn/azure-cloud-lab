# AZ-900 Domain 2: Core Azure Services

## 1. Compute Services (Which to Choose?)

- Azure Virtual Machines (VMs):
  - IaaS. Full OS control (Linux/Windows).
  - Use case: Legacy line-of-business software, custom OS kernel dependencies.
- Azure Virtual Machine Scale Sets (VMSS):
  - Automatically deploys and balances identical VMs.
  - Core mechanism behind autoscaling and elasticity.
- Azure App Service & Azure Static Web Apps:
  - PaaS. Fully managed web app runtime.
  - Static Web Apps: Built specifically for frontend frameworks (Next.js, React) and static sites with automated GitHub Actions CI/CD.
- Azure Containers:
  - Azure Container Instances (ACI): Fastest way to run an isolated container on-demand without managing a cluster (serverless container).
  - Azure Kubernetes Service (AKS): Full enterprise container orchestration, scaling, and service meshes.
- Azure Functions:
  - Serverless event-driven compute. Pay only for execution time (measured in milliseconds).

---

## 2. Azure Storage Services

- Blob Storage (Object Storage):
  - Stores unstructured data (images, video, backup archives, static site assets).
  - Tiers:
    - Hot: Frequently accessed, highest storage cost, lowest access cost.
    - Cool: Infrequently accessed (30-day minimum), lower storage cost, higher access fee.
    - Cold: Rare access (90-day minimum), significantly discounted storage.
    - Archive: Offline storage (180-day minimum, hours to rehydrate), cheapest storage rate.
- Azure Files:
  - Managed file shares accessible via SMB (Server Message Block) and NFS. Mountable directly on Windows, macOS, and Linux.
- Azure Disks:
  - Block-level storage attached to Virtual Machines (OS disks and Data disks).

---

## 3. Core Networking Architecture

- Azure Virtual Network (VNet):
  - Isolated private IP network within your subscription.
  - Subnets: Segment the VNet into targeted IP sub-ranges (e.g., frontend subnet, database subnet).
- Network Security Groups (NSGs):
  - Basic Layer 4 stateful packet-filtering firewall.
  - Uses prioritized rules (100 to 4096, lowest number wins) to allow/deny incoming and outgoing traffic by IP, port, and protocol.
- Azure Virtual Network Peering:
  - Links two separate VNets over Microsoft's high-speed backbone network without routing traffic over the public internet.
- Azure VPN Gateway & ExpressRoute:
  - VPN Gateway: Encrypted IPsec tunnel over the public internet connecting on-premises to Azure.
  - ExpressRoute: Private, dedicated fiber connection bypassing the public internet completely for maximum speed, security, and enterprise reliability.
