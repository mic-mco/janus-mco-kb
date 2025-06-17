---
title: "AWS: Add a VPC"
slug: aws-add-a-vpc
---

## About this task

This article will guide you through the process of adding a new VPC to an AWS environment.

## Before you begin

- Your AWS environment must already exist
- If you do not want to use the default values provided by the system, you must have the name and the CIDR you wish to assign to the new VPC

## Procedure

1. Click on the **Add VPC network** button. The **Add VPC network** page will appear.

2. Enter a name for the new VPC into the **Name** field, or accept the default.

3. Enter the desired CIDR for the new VPC into the **CIDR** field, or accept the default.

    - The CIDR expresses the size and range of IPs to use for defining the new VPC. See [VPCs](aws-vpcs.md) for more details.

    - The system will present an error if an invalid CIDR is provided.

4. Click **Submit**.

## Results

- The VPC is created, and can be used to add subnetworks
- It has the IP range specified by the CIDR
- The VPC is listed in the **Networking** tab
