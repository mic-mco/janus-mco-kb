---
title: "AWS: Add a subnetwork"
slug: aws-add-a-subnetwork
---

## About this task

This article will guide you through the process of adding a new subnetwork to your AWS VPC.

## Before you begin

- You must have a VPC in your AWS environment
- The IP range of the VPC must have a block that is not assigned to another subnetwork
- If you do not want to use the default values provided by the system, you must have the name, the IP range, and the AWS availability zone you wish to assign to the new subnetwork

## Procedure

1. Navigate to the desired environment, and click **Networking**.

2. Find the desired VPC, and click on the gear icon in the **Subnets** section. The **Subnets** page will appear.

3. Click the **Add subnetworks** button. The **Add subnetworks** page appears.

4. Enter a name for the new subnet into the **Name** field, or accept the default.

5. Enter the desired IP range, using CIDR notation, into the **CIDR** field.

    The CIDR of the subnetwork must exist entirely within the CIDR of the VPC, and it must not overlap the CIDR of any other subnetwork within the same VPC. See [Subnetworks](aws-subnetworks.md) for more information.

    The system will present an error if an invalid CIDR is provided.

6. Select the desired availability zone from the **Availability zone** popup menu, or accept the default.

7. Click the **Submit** button.

## Results

- The subnetwork is created, and can be used to add instances
- It has the IP range specified by the CIDR
- The subnetwork is listed in the **Subnets** screen of the VPC in which it was created
