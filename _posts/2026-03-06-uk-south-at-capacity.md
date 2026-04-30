---
id: 13
title: 'AI Ready Landing Zone'
date: '2026-03-06T00:00:00+00:00'
author: 'Michael Coutanche'
layout: post
hidden: true  # Custom variable to hide from lists  
published: true 
categories:
    - Articles
---
# THIS IS A DRAFT

----------------------------------------------------
 If your Azure workloads live in UK South, you need to read this.

Microsoft is under serious capacity pressure in UK South, one of their busiest European regions. New quota requests are no longer auto-approved, and customers are hitting AllocationFailed errors when trying to spin up, scale, or resize VMs. This isn't new, but it's getting worse as AI workloads pile pressure onto the same infrastructure.
 
Here's what IT leaders should be doing right now:
 
🔒 Lock in what you've got Autoscaling rules that deallocate VMs can leave you without capacity to get them back. Temporarily pause scale-in rules until the pressure eases.
 
📦 Reserve capacity before it's gone Microsoft's On Demand Capacity Reservations let you guarantee VM capacity in UK South. It's a commitment, but it beats a failed deployment at the worst possible time.
 
🔄 Pick the right VM sizes Newer SKUs hit limits first. Widely available families like Dv3 have better allocation success rates right now. And if you're still on legacy SKUs like Av1 or Dv1, it's time to upgrade anyway.
 
🌍 Know your alternatives UK West, Sweden Central, and Norway East are worth evaluating for non-sensitive workloads. Data residency rules your options, but options exist.
 
📊 Use Microsoft's Allocation Success Recommender Built into the Azure Portal, it tells you which VM sizes are likely to succeed in your region over the next 7 days. Free, fast, and massively underused.
 
The organisations feeling this most are the ones who assumed Azure would just work. The ones who'll be fine are planning now.
 
Happy to talk through any of this, it's something we're actively helping customers navigate at the moment.

hashtag#MicrosoftAzure hashtag#ITInfrastructure hashtag#CloudComputing

------------------------------------

We need a statement to speak to us if they need more guidance etc. 






UK South Capacity Constraints

Microsoft is currently experiencing capacity constraints in the Azure UK South region. As a result, availability for certain services, SKUs, and new deployments may be limited or temporarily restricted in this region.

To ensure continued service reliability and to support customer growth, we are actively directing new workloads and expansions to alternative Azure regions and datacentres, where sufficient capacity is available. This approach allows us to maintain our high standards for performance, resilience, and customer experience.

What this means for customers
Existing workloads running in UK South are not impacted and will continue to operate as expected.
New deployments, scale‑outs, or service enablement requests in UK South may be constrained or subject to approval.
Customers are encouraged to deploy new workloads in alternative Azure regions, such as UK West or other suitable European regions, based on workload requirements, data residency needs, and business continuity considerations.
Approved Alternative Azure Regions
Customers should deploy new workloads or capacity expansions to one of the following Microsoft‑approved alternative regions, selected based on latency, resiliency, and regulatory alignment:

Primary UK Option
UK West
Paired region with UK South
Suitable for:
Business continuity and disaster recovery (BCDR)
UK data residency requirements
Low‑latency UK‑based workloads
Recommended European Regions
West Europe (Netherlands)
High‑capacity strategic Azure region
Broad service and SKU availability
Commonly used for scale‑out and multi‑region architectures
North Europe (Ireland)
Strong alignment with UK workloads
Low network latency to the UK
Suitable for production and DR scenarios
France Central
Suitable for customers with EU data residency or regulatory requirements
Full Azure platform support
Germany West Central
High enterprise adoption
Strong compliance and sovereignty capabilities
Technical Impact Summary
Affected Scenarios
New Azure resource deployments in UK South
Compute scale‑out (VMs, VMSS, AKS node pools)
Certain PaaS service provisioning and SKU enablement
Subscription quota increase requests tied to UK South
Unaffected Scenarios
Existing production workloads in UK South
Runtime performance and SLA commitments
Cross‑region replication, backup, and DR operation
Recommended Architecture Patterns
Customers are advised to adopt or extend multi‑region and region‑pair architectures, including:

Active/Passive or Active/Active designs using UK West or EU regions
Azure Traffic Manager / Azure Front Door for regional routing
Azure Site Recovery (ASR) for VM‑based disaster recovery
Geo‑redundant storage (GRS / RA‑GRS) for data durability
Zone‑redundant services where supported in alternative regions

