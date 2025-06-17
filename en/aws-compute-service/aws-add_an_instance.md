---
title: "AWS: Add an instance"
slug: aws-add-an-instance
---

## About this task

This article will guide you through the process of adding a new instance to an AWS environment. The CloudMC interface provides a multi-step wizard for selecting a configuration, and the instance \(or instances\) will be created after the final step of the wizard.

## Before you begin

- You must have a VPC configured
- The VPC must have a subnetwork configured
- The subnetwork must have at least one IP address available
- The number of instances that should be initially deployed
- The maximum number of instances to allow when autoscaling

## Procedure

1. Navigate to the desired environment. The **Instances** page appears.

2. Click on the **Add instance** button. The **Add instance** wizard appears.

3. Configure the base settings for the instance.

    - Enter a name into the **Name** field, or accept the default.

    - Select the region where the instance is to be deployed.

    - Select the image to use for deploying the instance.

    - Select the desired instance type from the **Instance Type** popup menu.

    - Select the desired minimum and maximum number of instances to have deployed.

    Click **Next** to continue.

4. Configure the security settings for the instance.

    - Enter a name for the new SSH key pair into the **Key name** field, or accept the default.

    - Define a new security group for the instance, or select a pre-defined set.

    Click **Next** to continue.

5. Configure the networking settings for the instance.

    - From the **VPC** popup menu, select the VPC where the instance will be created.

    - From the **Subnetwork** popup menu, select the subnetwork where the instance will be created.

    Click **Next** to continue.

6. Configure the storage settings for the instance.

    On the **Storage Configuration** page, you can choose the settings for the root volume of the new instance.

    - Enter the desired device name for the volume into the **Device name** field, or accept the default.

    - Select the volume performance type from the **Volume type** popup menu.

    - Enter the size for the volume in gigabytes \(GB\) into the **Size** field.

    - If needed, select the **Delete on termination** checkbox.

    On this step, you can add multiple volumes with the **Add** button. Pressing this button will cause an additional volume configuration section to appear. Enter the desired parameters accordingly. When adding multiple volumes, the device name must be unique for each volume. Click the **Remove** button to eliminate that volume from the list.

    Click **Next** to continue.

7. Select any existing volumes to attach.

    On the **Attach existing volumes** page, you can attach volumes that already exist within the availability zone of the instance to be created.

    Multiple volumes can be attached to the new instance by clicking on the **Add** button. Ensure that each volume has a unique device name.

    - Select the volume to attach from the **Volumes** popup menu.

    - Enter the desired device name into the **Device name** field.

    Clicking the **Remove** button eliminates that volume from the list.

8. Click the **Submit** button.

    The wizard screen will close and you will be returned to the **Instances** screen of the **Compute** tab. It may take several moments for the instance to be added. During this time, the Notification panel will indicate that the instance is being created.

9. Save the private SSH key provided in the notification.

    - Click the **Bell** icon to expand the notification panel.

    - Identify the notification for your instance by searching for the instance name.

    - Click the **Clipboard** icon to copy the full private SSH key into your clipboard.

    - Store the private SSH key securely.

## Results

- The instance is created with the selected configuration options
- The number of instances created is the value provided in the **Minimum \# of instances** field
- The instance will be created in the availability zone of the selected subnetwork
- Any new volumes that were defined will be attached to the new instance
- Any existing volumes that were specified to the wizard will be attached to the new instance
- The instance is now listed in the **Instances** page of the **Compute** tab
- The private SSH key needed to log into the instance has been stored securely
