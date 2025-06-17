---
title: "Cloud 360: Add a disk"
slug: cloud360-add-a-disk
---

## About this task

This article will guide you through the process of adding a new disk to an already provisioned virtual machine in a TIGO Cloud 360 environment (VDC). The TIGO MCO interface provides a wizard to configure and deploy virtual disks.

## Before you begin

- Your TIGO Cloud 360 environment (VDC) must already exist.
- The virtual machine to which a new disk needs to be added must exist within the environment (VDC).

## Procedure

1. Navigate to the desired environment (VDC). The Virtual Machines page appears.

2. In the displayed list, locate the virtual machine to which the new disk will be added and click on it.

3. The page with the virtual machine's Details appears. Click on the Hard Disks option located in the menu on the left side of the page.

4. A list of disks currently associated with the virtual machine appears. The base disk (where the operating system is installed) and additional disks (if the virtual machine has them) should be shown.

5. Click the Add Disk button to start the deployment wizard.

    5.1. Enter the size of the disk to be created; you can select units in GB or MB.

    5.2 In the Bus type field, select the Paravirtual (SCSI) value.

    5.3 The values to be entered in the Bus number and Unit number fields are integers between 0 and 3. The base disk (where the operating system is installed) uses bus 0 and unit 0. You can choose any other combination according to your technical requirements. It is recommended to follow an order, for example, for the first additional disk use bus 0 and unit 1, for the second additional disk use bus 0 and unit 2, for the third disk use bus 0 and unit 3. In this sequence, the fourth disk would already use bus 1 and unit 1, and continue with this logic for more disks.

6. Click the Apply button.

7. The hard disk will be provisioned in the virtualizer. Additional actions within the operating system are required for this new disk to be usable. Consult the documentation for each operating system to obtain the list of actions to perform.

## Results

- The additional disk is provisioned and becomes available for configuration at the operating system level.
- The new disk will be displayed in the Hard Disks section.
