---
title: "Cloud 360: Add a NIC"
slug: cloud360-add-a-nic
---

## About this task

This article will guide you through the process of adding a new network interface to an already provisioned virtual machine in a TIGO Cloud 360 environment (VDC). The TIGO MCO interface provides a wizard to configure and deploy new network interfaces.

## Before you begin

- Your TIGO Cloud 360 environment (VDC) must already exist.
- The virtual machine to which the new network interface needs to be added must exist within the environment (VDC).

## Procedure

1. Navigate to the desired environment (VDC). The Virtual Machines page appears.

2. In the displayed list, locate the virtual machine to which the network interface will be added and click on it.

3. The page with the virtual machine's Details appears. Click on the Network Interface Controllers option located in the menu on the left side of the page.

4. A list of network interfaces currently associated with the virtual machine appears. It is possible that no network interfaces are associated with the virtual machine, which would mean the machine is isolated from other machines within the environment (VDC) and even from external connectivity (Internet, MPLS).

5. Click the Add NIC button to start the deployment wizard.

    5.1 In the Network field, all available networks within the environment (VDC) will be listed. Select the network you want to associate with the new network interface.

    5.2 Select the Primary checkbox only if you wish to set the new network interface as the primary one for the virtual machine.

    5.3 If you want to associate the new network interface with a network different from those available, you must first create the new network. Refer to the article Cloud 360: Add a Network for more details on how to create a new network.

6. Click the Apply button.

7. The new network interface will be provisioned in the virtualizer. Additional actions within the operating system are required for this new interface to be usable. Consult the documentation for each operating system to obtain the list of actions to perform.

## Results

- The network interface is provisioned and becomes available for configuration at the operating system level.
- The new network interface will be displayed in the Network Interface Controllers section.
