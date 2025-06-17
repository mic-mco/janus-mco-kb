---
title: "Using environments to organize users and workloads"
slug: environments-to-organize-workloads-and-users
---

### Environments overview

The platform provides a powerful mechanism, **environments**, to segregate workloads and resources, and to control who gets access to those. Example use-cases of this concept include creating distinct environments to isolate production workloads from development systems, or establishing project-specific [sandboxes](https://en.wikipedia.org/wiki/Sandbox_%28computer_security%29).

An environment belongs to an organization, is associated with a specific service (e.g. Compute or Object Storage), and is comprised of a set of members who have visibility on a pool of shared resources, such as instances, storage, etc.  Members are users that have been granted access to a given environment.  A user in an organization is not necessarily a member of the environments in that organization.

### Create an environment

Any user with the **User** role, or any other role which has the *Environments: Create* permission, can add additional environments and decide who should have access to it.

1. Click on *Add environment*.  The *Add environment* page will appear.
1. Enter a name and an optional description for the environment.
1. If you wish to allow users from other organizations to be added as members, select **Allow external members**.
1. Click *Next*.  The environment will be provisioned.
1. The *Manage members* page will appear momentarily.  Here, you may:
   - Select one or more individual users from the list
   - Search for specific users
   - Add **all users** in the organization (**auto-membership**)
   - Add no users to your environment (click *Skip* to proceed to the next page)
1. For any users you've added, select an environment role.  If you've enabled auto-membership, select a default environment role.
1. Click *Apply* to commit the selected members.  The users will be added.
