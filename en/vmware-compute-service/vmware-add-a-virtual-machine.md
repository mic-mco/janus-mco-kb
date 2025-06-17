---
title: "Cloud 360: Add a virtual machine"
slug: cloud360-add-virtual-machine
---

## About this task

This article will guide you through the process of adding a new virtual machine to a TIGO Cloud 360 environment (VDC).

## Before you begin

- You must have a network already realized in your TIGO Cloud 360 environment (VDC)

## Procedure

1. Navigate to the desired environment. The **Virtual Machines** page appears.

2. Click on the **Add Virtual Machine** buttton. The **Add Virtual Machine** wizard appears.

3. Enter a name for the new virtual machine in the **Name** field, or accept the default.

4. To have the virtual machine automatically power on at creation time, mark the **Power On** checkbox.

5. If you wish to have the virtual machine be a part of an existing virtual application, select the desired application from the **Virtual Application** popup menu.

6. Select from the **Network** popup menu which network to attach the new virtual machine to, or accept the default.

7. Select the required option from a set of templates with various operating systems and versions already installed. Additionally, select the default memory and vCPU sizes available within the **Virtual Machine Sizing Policy** option

8. Click the **Submit** button to create the new virtual machine.

## Results

- The virtual machine is created using the specified settings
- If **Power On** was selected, the system starts the virtual machine immediately after creating it
- The virtual machine is listed in the **Virtual Machines** screen

**Important:** You must securely store the administrator access password. It will not be stored anywhere in the TIGO MCO user interface and cannot be recovered once the dashboard notification is dismissed. You cannot log in to the virtual machine's operating system without this key. If lost, you will need to follow a recovery procedure, which may involve restarting the virtual machine.
