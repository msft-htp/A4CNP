# Azure Landing Zone Whiteboard

Time to put your architect hat on and exercise everything you just learned by designing an ALZ solution.

## Instructions

### Duration
90 minutes
- 75 designing solution
- 15 sharing solutions across teams
  
### Task
Work together as a team by leveraging the information you just learned, links to resources below, and the avaialble Azure SMEs to design an Azure Landing Zone solution addressing Contoso DB, Inc’s requirements below.

> NOTE: Any seasoned architect will tell you, "it depends," when asked how a solution should be designed. The same applies to this challenge - there is not a single "correct" answer.

## Challenge

### About Contoso DB, Inc

*Contoso DB, Inc* is the cloud native company behind the wildly popular NoSQL DB that finally solved one of NoSQLs biggest limitations - fast, scalable, multi-collection ACID transactions. They started as an OSS project and eventually moved to a freemium model in order to offer enterprise support and other value added services and products.

Although *Contoso DB, Inc* has had success growing revenue via their AWS, Azure, and GCP IaaS marketplace offerings, internal market research shows there is high demand for a fully managed SaaS offering. The research also shows equal demand for the SaaS solution across AWS and Azure customers; however, they don't have in-house expertise to build a secure and scalable SaaS offering in Azure...yet.

### Your Role and Mission (should you accept it)

Congratulations! You and your team were just hired as *Contoso DB, Inc's* Azure Architecture/Engineering teams. You have been tasked with designing a scalable and sustainable Azure environment for your Contoso DB SaaS product as well as the various planned internal IT applications.

The CTO recognizes there will be several iterations of the design as new requirements and considerations are discovered. For the first iteration, she is interested in the following design considerations:

- Azure AD Tenant Design (can we use a single Azure AD tenant or do we need two - one for IT and one for SaaS)
- Management group design
- Subscription design (both internal IT and multi-tenent SaaS)
- Thoughts on whether or not to use Azure Policy to implement security controls and if so, which policies/initiatives might make sense for initial design
- High-level RBAC design
- High-level network design

The CTO has also heard about the Azure Landing Zone accelerators and wants your opinion on whether an accelerator could be used as a starting point for your greenfield Azure environment.

### Stakeholders (and their requirements)

- CTO
  - Ensure the new greenfield Azure environment is scalable, sustainable, and adaptable to changing needs of the business
  - Keep *Contoso DB, Inc* out of the news...
  - Ensure *Contoso DB, Inc's* Azure environment is 800-171 R2 compliant
- CISO
  - *Contoso DB, Inc's* data is segregated from customer data
  - Maintain high degree of isolation between SaaS tenants
  - No standing access to the Azure environment
  - Ability to quickly detect and respond to anomalous signals
  - Keep *Contoso DB, Inc* out of the news...
- CFO
  - Minimize COGS
  - Ability to roll-up Azure internal IT and SaaS costs separately
- Cloud Infrastructure Engineering Team
  - Avoid "click-ops" at all costs
  - Just enough access
- Cloud Security Engineering Team
  - Prevent engineering teams from accidentally misconfiguring cloud resources
  - Leverage Azure native services to identify and report security vulnerabilities
- Networking Team
  - Ensure SaaS service is "airgapped" from *Contoso DB, Inc's* IT Azure environment
  - Ensure strict network ingress/egress
- SaaS application developer teams
  - Dev environment with console access (Portal, CLI, etc)
  - CI/CD pipelines to deploy code
  - Observability of SaaS environment
- Customer Support Team
  - Just-in-time access to customer resources

### Resources

The following resources may help you as you work through your design.

- [What is an Azure Landing Zone?](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/)
- [Independent software vendor (ISV) considerations for Azure landing zones](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/isv-landing-zone)
- [Azure Landing Zone reference implementations](https://github.com/Azure/Enterprise-Scale/blob/main/docs/EnterpriseScale-Deploy-reference-implentations.md)
- [Architect multitenant solutions on Azure](https://learn.microsoft.com/en-us/azure/architecture/guide/multitenant/overview)
- [ALZ Management groups](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/design-area/resource-org-management-groups)
- [ALZ Subscriptions considerations and recommendations](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/design-area/resource-org-subscriptions)
- [Adopt policy-driven guardrails](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/enterprise-scale/dine-guidance)
- [Azure Policy built-in policy definitions](https://learn.microsoft.com/en-us/azure/governance/policy/samples/built-in-policies)
- [NIST SP 800-171 R2 Regulatory Compliance built-in initiative](https://learn.microsoft.com/en-us/azure/governance/policy/samples/nist-sp-800-171-r2)
- [Identity for Azure platform resources](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/design-area/identity-access-platform-access)
- [Azure built-in Roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)
- [Define an Azure network topology](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/define-an-azure-network-topology)
- [Plan for inbound and outbound internet connectivity](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/plan-for-inbound-and-outbound-internet-connectivity)
- [Microsoft Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/architecture/framework/)
- [What is Azure AD Privileged Identity Management?](https://learn.microsoft.com/en-us/azure/active-directory/privileged-identity-management/pim-configure)
