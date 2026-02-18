---
id: 12
title: 'Upcoming Change: Unmanaged Disk Support Ending 31st March 2026!'
date: '2026-02-13T00:00:00+00:00'
author: 'Michael Coutanche'
layout: post
hidden: false  # Custom variable to hide from lists  
published: true 
categories:
    - Articles
---
# THIS IS A DRAFT - TEST - UPDATE IMAGES

**WARNING:** Starting April 1, 2026, Azure IaaS virtual machines that rely on unmanaged disks will no longer be able to start. If any of these VMs are still running or allocated at that time, Azure will automatically stop and deallocate them. This change marks the next step in Microsoft’s move toward fully managed, more resilient disk options—so now’s the time to migrate any remaining unmanaged disks to managed disks to avoid service interruptions.



https://learn.microsoft.com/en-us/azure/virtual-machines/unmanaged-disks-deprecation

Quick check: Azure Portal → VMs → filter "Uses managed disks = No"

If anything shows up - you have 6 weeks.

The migration itself is simple (stop VM, convert, restart - minutes per VM), but planning maintenance windows across a production environment takes time.

Don't wait until March to find out.