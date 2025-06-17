---
title: "Allow outbound communication in TIGO Cloud 360"
slug: outbound-internet-cloud360
---

TIGO Cloud 360 environments (VDCs) have the capability to establish connections to and from the Internet. This article describes the configurations required to allow outbound Internet communication from all virtual machines sharing the same network, or from only a particular virtual machine.

### Initial Steps

Navigate to the desired environment (VDC) where the **Virtual Machines** section will appear. Select the **Networks** option and, subsequently, the **EDGE Gateway** option. All EDGE devices available for the current environment (VDC) will be displayed. In most cases, only one EDGE device will exist.

All necessary configurations to allow outbound Internet communication will be performed within the EDGE device.

![EDGE management main screen](/assets/vmware-edge-es.png)

### Create NAT Rule

Click on the gear icon for the **NAT Rules** section within the EDGE device. This will display a list of the currently configured NAT rules. The list may appear empty if it's the first NAT rule being generated, or if a complete deletion of rules was performed.

Click the **Add NAT Rule** button located on the right side of the page; this action will start the new rule configuration wizard.

Enter a descriptive name for this rule. In the **Type** field, select the SNAT option.
Automatically, the system will assign the EDGE's Public IP in the **External IPs** field. Do not make changes to this value.
In the **Internal IPs** field, you can specify a specific IP or a range of IPs. This IP or range of IPs will be those that have outbound Internet access through this rule.

Let's assume that the network 192.168.12.1/25 is configured in your environment and that one of the provisioned virtual machines has the IP 192.168.12.10 assigned. If you wish to grant Internet access to any virtual machine (currently provisioned or to be provisioned in the future) that has an interface in this network, you should then enter 192.168.12.1/25 as the value in the **Internal IPs** field. If you only want to allow Internet access to a particular virtual machine, you should enter the specific IP as the value. In our example case, the value to enter would be 192.168.12.10/32.

Click **Apply** to create the NAT rule.

![Configuration example of a NAT rule](/assets/vmware-nat-rule-in-es.png)

### Create IP Set

An IP set is a group of IP addresses that can be used as sources and destinations in firewall rules. An IP set can contain a combination of individual IP addresses, IP ranges, and subnets.

Navigate back to the EDGE device configuration screen. Click on the gear icon for the **IP Sets** section. This will display a list of the currently configured IP sets. The list may appear empty if it's the first set being generated, or if a complete deletion of sets was performed.

Click the **Add an IP Set** button located on the right side of the page; this action will start the new set configuration wizard.

Enter a descriptive name for this set and, optionally, a detailed description. If you intend to grant Internet access to an entire network segment, you can choose to select the CIDR Network value from the **Type** field and select the network in question from the **CIDR Network** dropdown field. If you intend to grant Internet access only to a single virtual machine, you can choose to select the Manual value from the **Type** field and enter the virtual machine's IP in the **IP Addresses** field; in our example, the value to assign would be 192.168.12.10/32.

Click **Apply** to create the IP set.

![Configuration example of an IP set](/assets/vmware-ip-set-in-es.png)

### Create Firewall Rule

Navigate back to the EDGE device configuration screen. Click on the gear icon for the **Firewall Rules** section. This will display a list of the currently configured firewall rules. This list will contain, at a minimum, the default rule which is a drop from ANY to ANY. This rule cannot be deleted, as it is a protective measure to discard all traffic that does not have an explicit allow rule.

Click the **Add Firewall Rule** button located on the right side of the page; this action will start the new firewall rule configuration wizard.

Enter a descriptive name for this rule. Ensure that the **Enabled** checkbox is selected. In the **Priority** field, select the Top value. Keep in mind that the priority assigned to a rule directly influences the outcome. If a firewall rule that allows communication is below a rule that does not allow that same communication, then the communication will not be established.

In the **Source** field, select the name of the newly created IP set and, in the destination field, select the Any value. The action field must have the value Allow. In our example, we are working with IPv4; therefore, this value must be selected in the **IP Protocol** field.

Click **Apply** to create the firewall rule.

![Configuration example of a FW rule](/assets/vmware-fw-rule-in-es.png)

From the operating system of a virtual machine within the network segment associated with the NAT rule and the IP set, confirm Internet connectivity using a Web browser, a ping command to an Internet server IP, or any other available and preferred method.
