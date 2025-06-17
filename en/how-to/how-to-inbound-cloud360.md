---
title: "Allow inbound communication in TIGO Cloud 360"
slug: inboud-internet-cloud360
---

TIGO Cloud 360 environments (VDCs) have the capability to establish connections to and from the Internet. This article describes the configurations required to publish a port to the Internet and allow inbound communication. Specifically, it addresses how to publish port 443 (HTTPS) for a Web page.

### Initial Steps

Navigate to the desired environment (VDC) where the **Virtual Machines** section will appear. Select the **Networks** option and, subsequently, the **EDGE Gateway** option. All EDGE devices available for the current environment (VDC) will be displayed. In most cases, only one EDGE device will exist.

All necessary configurations to allow inbound communication from the Internet will be performed within the EDGE device.

![EDGE management main screen](/assets/vmware-edge-es.png)

### Create NAT Rule

Click on the gear icon for the **NAT Rules** section within the EDGE device. This will display a list of the currently configured NAT rules. The list may appear empty if it's the first NAT rule being generated, or if a complete deletion of rules was performed.

Click the **Add NAT Rule** button located on the right side of the page; this action will start the new rule configuration wizard.

Enter a descriptive name for this rule. In the **Type** field, select the DNAT option.
Automatically, the system will assign the EDGE's Public IP in the **External IPs** field. Do not make changes to this value.
In the **Internal IPs** field, you can specify a specific IP, which in this case, corresponds to the address associated with the virtual machine where the Web service to be published resides. Let's assume the IP of this machine is 192.168.12.10/32.

In the **External Port** field, we can specify a custom port for the service if the real service port is not desired. For our example, this field will be left blank.

Select the value HTTPS - TCP: 443 from the list associated with the **Application** field.

Click Apply to create the NAT rule.

![Configuration example of NAT rule](/assets/vmware-nat-rule-out-es.png)

### Create IP Set

An IP set is a group of IP addresses that can be used as sources and destinations in firewall rules. An IP set can contain a combination of individual IP addresses, IP ranges, and subnets.

Navigate back to the EDGE device configuration screen. Click on the gear icon for the **IP Sets** section. This will display a list of the currently configured IP sets. The list may appear empty if it's the first set being generated, or if a complete deletion of sets was performed.

Click the **Add an IP Set** button located on the right side of the page; this action will start the new set configuration wizard.

Enter a descriptive name for this set and, optionally, a detailed description. If you intend to grant Internet access to an entire network segment, you can choose to select the CIDR Network value from the **Type** field and select the network in question from the **CIDR Network** dropdown field. If you intend to grant Internet access only to a single virtual machine, you can choose to select the Manual value from the **Type** field and enter the virtual machine's IP in the **IP Addresses** field; in our example, the value to assign would be the Web server's IP, i.e., 192.168.12.10/32.

Click **Apply** to create the IP set.

### Create Firewall Rule

Navigate back to the EDGE device configuration screen. Click on the gear icon for the **Firewall Rules** section. This will display a list of the currently configured firewall rules. This list will contain, at a minimum, the default rule which is a drop from ANY to ANY. This rule cannot be deleted, as it is a protective measure to discard all traffic that does not have an explicit allow rule.

Click the **Add Firewall Rule** button located on the right side of the page; this action will start the new firewall rule configuration wizard.

Enter a descriptive name for this rule. Ensure that the **Enabled** checkbox is selected. In the **Priority** field, select the Top value. Keep in mind that the priority assigned to a rule directly influences the outcome. If a firewall rule that allows communication is below a rule that does not allow that same communication, then the communication will not be established.

In the **Source** field, select the Any value to allow access from any location on the Internet. If you want to limit access only to certain IPs, you must first create the IP set. In the destination field, select the name of the newly created IP set. The action field must have the value Allow. In our example, we are working with IPv4, therefore, this value must be selected in the **IP Protocol** field.

Click **Apply** to create the firewall rule.

![Configuration example of a FW rule](/assets/vmware-fw-rule-out-es.png)

Confirm the result by accessing the Web portal from the Internet.
