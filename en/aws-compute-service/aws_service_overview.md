---
title: "AWS: Service overview"
slug: aws-service-overview
---

## Summary

TIGO MCO allows cloud operators to access and manage infrastructure and resources that have been deployed on the Amazon Web Services \(AWS\) platform. This article will introduce basic concepts of AWS and working with AWS resources in TIGO MCO.

## Detailed overview

The AWS platform is a public cloud, where customers can allocate resources to build an infrastructure for their applications. TIGO MCO provides a unified interface to access AWS and other services from a single portal. Through TIGO MCO, users can manage:

- [Compute and storage resources](aws-compute.md):
  - [Instances](aws-instances.md)
  - [Amazon Machine Images \(AMIs\)](aws-amis.md)
  - [Volumes](aws-volumes.md)
- [Networking resources](aws-networking.md):
  - [VPCs](aws-vpcs.md)
  - [Subnetworks](aws-subnetworks.md)
- [Object storage resources](aws-object_storage.md)

Because TIGO MCO acts as a portal to AWS services, you may find that some operations appear to behave differently than when interacting with AWS directly. However, behind the scenes, all operations execute exactly as they normally would. Changes made to AWS entities in CloudMC will be reflected immediately in the actual resources.
