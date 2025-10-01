---
id: 2
title: 'WBroadcom VMware Licensing Changes: What Azure VMware Solution Customers Need to Know'
date: '2025-09-05T00:00:00+00:00'
author: 'Michael Coutanche'
tags: [Azure, VMware, Licensing, Migration, Cloud]
layout: post
categories:
    - Articles
---

# Broadcom VMware Licensing Changes: What Azure VMware Solution Customers Need to Know

*By Michael Coutanche, Azure Practice Lead & Microsoft Partner MSP*

## Introduction

The cloud landscape is shifting rapidly, and nowhere is this more evident than in the recent changes to VMware licensing under Broadcom’s stewardship. If you’re running workloads on Azure VMware Solution (AVS), it’s crucial to understand how these changes will impact your licensing, procurement, and operational strategy from November 1, 2025.

## What’s Changing?

Broadcom is moving all hyperscaler platforms—including Azure VMware Solution—to a **“bring your own” portable subscription** model for VMware Cloud Foundation (VCF):

- **Customers must purchase portable VCF subscriptions directly from Broadcom or its authorized channel partners.**
- Microsoft will no longer bundle VCF licenses with AVS node purchases after October 15, 2025.
- Existing AVS Reserved Instances (RIs) purchased on or before October 15, 2025, will remain valid until the end of their term.
- PayGo nodes with license included can continue to operate until October 31, 2026, after which a BYOL model is mandatory.
- No product changes to AVS—Microsoft continues to manage infrastructure, patching, and upgrades.[1](https://techcommunity.microsoft.com/blog/azuremigrationblog/broadcom-vmware-licensing-changes-what-azure-vmware-solution-customers-need-to-k/4448784)

## Why Is This Happening?

Broadcom’s strategy is to simplify and streamline VMware’s portfolio, focusing on subscription-based licensing and license portability. This shift is designed to give customers more flexibility to move workloads between on-premises and cloud environments, but it also introduces new procurement and compliance requirements.[2](https://www.schneider.im/vmware-by-broadcom-portfolio-simplification-and-transition-to-subscription/)

## What Does This Mean for Azure VMware Solution Customers?

- **No Product Changes:** AVS remains a fully managed VCF private cloud service. Microsoft continues to handle infrastructure, patching, and upgrades.
- **Licensing Complexity:** Customers must manage their own VCF licenses, which can add administrative overhead, especially for large or hybrid environments.
- **Strategic Planning Required:** Organizations should inventory their current AVS nodes, evaluate RI terms, and plan future purchases to avoid running out of valid licenses.[3](https://besharpexperts.com/en/wat-azure-vmware-solution-klanten-moeten-weten-over-de-broadcom-licentiewijzigingen-per-1-november-2025/)

## Key Dates & Actions

- **October 15, 2025:** Last day to purchase AVS nodes with bundled VCF licenses.
- **November 1, 2025:** All new AVS node purchases require BYOL VCF subscriptions.
- **October 31, 2026:** End of support for PayGo nodes with bundled licenses.

## How to Purchase VCF Subscriptions

- VCF subscriptions must be purchased directly from Broadcom or authorized channel partners. If you don’t have a Broadcom contract, leverage their partner ecosystem for procurement support.
- Register your portable VCF license with Microsoft to use it with AVS. Ensure your license covers all physical cores in your AVS hosts.[4](https://learn.microsoft.com/en-us/azure/azure-vmware/vmware-cloud-foundations-license-portability)

## Reserved Instances: Lock in Value

If you have existing Reserved Instances, you’re protected until your RI term ends. Consider extending your RI term before October 15, 2025, to lock in current pricing and licensing models. After this date, all new purchases require BYOL.[5](https://azurefeeds.com/2025/09/10/broadcom-vmware-licensing-changes-what-azure-vmware-solution-partners-need-to-know/)

## Storage Optimization Matters

With licensing now tied to per-core usage, optimizing your AVS infrastructure—especially storage—is more critical than ever. Overprovisioned storage can inflate licensing costs. Solutions like Pure Cloud Block Store for AVS can help drive efficiency and reduce your footprint.[6](https://blog.purestorage.com/perspectives/broadcoms-vcf-licensing-shift-avs-customers/)

---

## Azure VMware Solution Architecture Diagram

Below is a simplified architecture diagram for Azure VMware Solution, showing connectivity between on-premises, AVS, and native Azure services:

![Azure VMware Solution Architecture](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/azure-vmware/example-architectures)  
*Source: Microsoft Learn*[7](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/azure-vmware/example-architectures)

---

## Migration Tips

1. **Assess Your Current Environment:** Inventory all AVS nodes and determine which use bundled licenses, PayGo, or Reserved Instances.
2. **Evaluate Reserved Instances:** Take advantage of existing RI terms and plan future purchases carefully. Extend RI terms before October 15, 2025, if possible.
3. **Plan for License Portability:** Ensure you have a Broadcom contract or channel partner relationship to purchase VCF licenses.
4. **Optimize Infrastructure:** Review storage and compute allocations to minimize licensing costs. Consider consolidating workloads or leveraging storage solutions like Pure Cloud Block Store.
5. **Test Compatibility:** Before deploying new nodes, verify your VCF subscription covers all required cores and add-ons (e.g., vDefend Firewall).
6. **Leverage Azure Migrate:** Use Azure Migrate and related tools to benchmark TCO and streamline migration to AVS or Azure Native services.
7. **Engage Stakeholders:** Communicate changes to IT, procurement, and finance teams to ensure compliance and budget planning.
8. **Monitor Updates:** Stay informed via Microsoft Tech Community and Broadcom announcements for any further changes or guidance.

---

## Frequently Asked Questions (FAQ)

**Q: What is the Broadcom licensing change for AVS?**  
A: Starting November 1, 2025, customers must bring their own portable VCF subscription purchased from Broadcom to use AVS. Microsoft will no longer bundle VCF licenses with AVS node purchases.[1](https://techcommunity.microsoft.com/blog/azuremigrationblog/broadcom-vmware-licensing-changes-what-azure-vmware-solution-customers-need-to-k/4448784)

**Q: Will my existing AVS Reserved Instances be affected?**  
A: No, Reserved Instances purchased on or before October 15, 2025, will remain valid until the end of their term.[5](https://azurefeeds.com/2025/09/10/broadcom-vmware-licensing-changes-what-azure-vmware-solution-partners-need-to-know/)

**Q: How do I purchase a VCF subscription for AVS?**  
A: VCF subscriptions must be purchased directly from Broadcom or authorized channel partners. Register your license with Microsoft to use it with AVS.[4](https://learn.microsoft.com/en-us/azure/azure-vmware/vmware-cloud-foundations-license-portability)

**Q: What happens to PayGo nodes?**  
A: PayGo nodes with license included can continue to operate until October 31, 2026. After that, BYOL is required.[3](https://besharpexperts.com/en/wat-azure-vmware-solution-klanten-moeten-weten-over-de-broadcom-licentiewijzigingen-per-1-november-2025/)

**Q: Are there any product changes to AVS?**  
A: No, these updates are licensing-only. AVS remains a fully managed VCF private cloud service.[8](https://www.directionsonmicrosoft.com/broadcom-inserts-itself-into-azure-vmware-solution/)

**Q: What add-ons do I need for AVS?**  
A: If you use features like vDefend Firewall, you must purchase the add-on from Broadcom and register it with Microsoft.[4](https://learn.microsoft.com/en-us/azure/azure-vmware/vmware-cloud-foundations-license-portability)

**Q: How do I optimize my AVS environment for licensing?**  
A: Review your infrastructure for overprovisioned storage and compute. Optimize workloads and consider storage solutions to reduce your licensing footprint.[6](https://blog.purestorage.com/perspectives/broadcoms-vcf-licensing-shift-avs-customers/)

---

## Helpful Resources

- [Microsoft Tech Community: Broadcom VMware Licensing Changes](https://techcommunity.microsoft.com/blog/azuremigrationblog/broadcom-vmware-licensing-changes-what-azure-vmware-solution-customers-need-to-k/4448784)[1](https://techcommunity.microsoft.com/blog/azuremigrationblog/broadcom-vmware-licensing-changes-what-azure-vmware-solution-customers-need-to-k/4448784)
- [Azure Docs: Use Portable VCF on AVS](https://learn.microsoft.com/en-us/azure/azure-vmware/vmware-cloud-foundations-license-portability)[4](https://learn.microsoft.com/en-us/azure/azure-vmware/vmware-cloud-foundations-license-portability)
- [Broadcom Blog: VCF Licensing Changes](https://blogs.vmware.com/cloud-foundation/2025/08/29/vmware-cloud-foundation-cloud-on-your-terms/)[2](https://www.schneider.im/vmware-by-broadcom-portfolio-simplification-and-transition-to-subscription/)
- [Pure Storage: Navigating Broadcom's VCF Licensing Changes](https://blog.purestorage.com/perspectives/broadcoms-vcf-licensing-shift-avs-customers/)[6](https://blog.purestorage.com/perspectives/broadcoms-vcf-licensing-shift-avs-customers/)

---

*Michael Coutanche is Practice Lead Azure at a leading Microsoft partner and Azure expert MSP. For more technical insights, follow techkb.onl.*

