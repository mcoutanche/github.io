---
id: 12
title: 'Upcoming Change! Unmanaged Disk Support Ending'
date: '2026-02-13T00:00:00+00:00'
author: 'Michael Coutanche'
layout: post
hidden: false  # Custom variable to hide from lists  
published: true 
categories:
    - Articles
---




**WARNING:** Starting April 1, 2026, Azure IaaS virtual machines that rely on unmanaged disks will no longer be able to start. If any of these VMs are still running or allocated at that time, Azure will automatically stop and deallocate them. This change marks the next step in Microsoft’s move toward fully managed, more resilient disk options—so now’s the time to migrate any remaining unmanaged disks to managed disks to avoid service interruptions.

<img src="{{ site.baseurl }}/assets/img/2026/02/2026-02-13-image-001.png" alt="Unmanaged Disks Depricated" style="max-width: 50%; height: auto; float: right;">


As Azure evolves its infrastructure services, Microsoft is retiring unmanaged disks in favour of managed disks, which have fully replaced the legacy architecture since their introduction in 2017. The new retirement deadline is March 31, 2026, extended from September 30, 2025. After this date, VMs using unmanaged disks cannot start, and any running VMs will be stopped and deallocated.

This retirement applies specifically to page blobs used as VHDs attached to VMs. However, workloads using page blobs only through REST APIs—and not as VM disks—are unaffected, an important distinction for organisations using storage‑driven architectures outside of VM scenarios.

Most organisations now need to prioritise migration planning. Managed disks offer clearer operational benefits: improved availability, simplified management, and access to larger and more performant disk types. Azure provides supported migration options for standalone VMs, availability sets, and classic‑to‑ARM transitions. Administrators should identify affected workloads using portal filtering or Azure Resource Graph queries.

Cost impacts vary: managed disks are billed on provisioned size, not consumed capacity, so right‑sizing is recommended before migration. The Azure Pricing Calculator can help model expected cost changes and guide budget planning.

With the retirement date approaching, teams should validate migration procedures, test conversions, and build a structured plan. Moving to managed disks ensures long‑term compatibility with Azure’s roadmap and provides a more stable and scalable infrastructure foundation.

**How to Update to Managed Disks**
Migrating a VM requires a brief maintenance window. For single-instance VMs, Azure’s commands convert the OS disk and attached data disks after the VM is deallocated; once conversion is complete, the VM restarts on managed disks. For availability sets, the set must be converted first before migrating the VMs.

Post‑migration, the original VHD page blobs and storage accounts remain and continue to incur charges. These must be manually deleted after verifying a successful migration. Azure’s portal and PowerShell tools make identifying and removing unused artifacts straightforward, ensuring both smooth migration and cost hygiene.

## Helpful Resources  

- [Microsoft Learn: Migrate your Azure unmanaged disks by March 31, 2026](https://learn.microsoft.com/en-us/azure/virtual-machines/unmanaged-disks-deprecation)
- [Microsoft Q&A](https://learn.microsoft.com/en-us/answers/tags/94/azure-virtual-machines)

