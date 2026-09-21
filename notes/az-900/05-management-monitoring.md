# AZ-900 Domain 3: Management, Monitoring & Cost Governance

## 1. Cost Planning & Management Tools

- Azure Pricing Calculator:
  - Estimates projected cloud costs before deploying resources.
- Total Cost of Ownership (TCO) Calculator:
  - Compares the operational cost of on-premises datacenter hardware against migrating to Azure over 3–5 years.
- Microsoft Cost Management:
  - Tracks historical and live cloud spend, sets spending budgets, and configures email billing alerts.
- Cost Optimization Factors:
  - Azure Reservations: 1-year or 3-year commitment on compute for deep discounts (up to 72%).
  - Azure Hybrid Benefit: Apply existing on-premises Windows Server / SQL Server licenses to Azure VMs.
  - Resource Tags: Key-value metadata pairs applied to resources (e.g., `Environment: Production`, `Owner: Glenn`) for cost center billing attribution.

---

## 2. Monitoring & Health Services

- Azure Monitor:
  - Comprehensive telemetry platform collecting Metrics (numerical real-time data) and Logs (event logs stored in Log Analytics).
  - Application Insights: Sub-feature monitoring live web app performance, page loads, and unhandled runtime exceptions.
  - Alert Rules: Sends emails, SMS, or triggers automated webhooks when metrics breach thresholds.
- Azure Service Health:
  - Personalized dashboard tracking Microsoft global cloud status:
    1. Azure Status: Global health across all regions.
    2. Service Health: Outages or degradation specifically impacting your subscription's active regions.
    3. Resource Health: Pinpoints whether an outage is caused by Azure datacenter issues or your own misconfiguration.
- Azure Advisor:
  - AI-driven recommendation engine analyzing resource telemetry across 5 pillars:
    1. Cost (e.g., identifies idle VMs)
    2. Security (integrates with Defender for Cloud)
    3. Reliability (HA gaps)
    4. Performance (bottlenecks)
    5. Operational Excellence (deployment hygiene)

---

## 3. Deployment & Infrastructure Management Tools

- Azure Resource Manager (ARM):
  - The unified management layer handling all Azure Portal, CLI, PowerShell, and SDK requests.
- Infrastructure as Code (IaC):
  - ARM Templates: JSON-based declarative templates.
  - Bicep: Azure's domain-specific language (DSL) providing clean, human-readable syntax that compiles directly into ARM JSON.
- Azure Command-Line Interfaces:
  - Azure CLI (`az`): Cross-platform Bash/Zsh scripting utility.
  - Azure PowerShell (`Az` module): Cmdlet-driven scripting for Windows PowerShell or PowerShell Core.
  - Azure Cloud Shell: Browser-accessible, authenticated terminal preloaded with CLI, PowerShell, Git, and Docker.
- Azure Arc:
  - Extends Azure Resource Manager governance, Azure Policy, and monitoring to non-Azure servers (on-premises physical hardware, AWS, Google Cloud).
