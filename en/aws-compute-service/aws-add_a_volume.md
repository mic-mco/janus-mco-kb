---
title: "AWS: Add a volume"
slug: aws-add-a-volume
---

## About this task

This article will guide you through the process of adding a new volume to an AWS environment.

## Before you begin

- Your AWS environment must already exist

## Procedure

1. Navigate to the desired environment. The **Instances** page appears.

2. Click on the **Volumes** item. A list of volumes in this environment appears.

3. Click on the **Add Volume** button. The **Add Volume** wizard appears.

4. Configure the new volume:

    1. Enter a name into the **Name** field, or accept the default.

    2. Select the volume type to create.

    3. Enter the number of gigabytes to allocate for the new volume into the **Size** text box. The volume must be an integer.

    4. Select the availability zone where the new volume should be created.

        The choice of availability zone will determine the instances to which the new volume may be attached.

5. \(Optional\) You can automatically attach the new volume to an existing instance:

    1. Click on **Attach volume to existing instance**.

    2. A list of instances in the selected availability zone will appear. Select the desired instance.

    3. Enter the desired device name into the text box labeled **Device Name**.

6. Click the **Submit** button.

## Results

- The volume of the specified size is created in the active environment
- It exists in the selected availability zone
- If an instance was selected, the volume is automatically attached to that instance
- The volume is listed in the **Volumes** screen of the **Compute** tab
