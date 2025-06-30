# Deployment Overview

A deployment is a higher-level object that manages and automates the lifecycle of a set of replicated pods

* One of the mode commonly used K8 resources for managing stateless applications
* Provides users with the capability to upgrade the underlying instances seamlessly using roling updates,undo changes, and pause and resume changes as required

<br>

# Deployment Revision

* Helps users keep track of the changes made to their deployment
* Enables users to rollback to a previous version if needed

<br>

# Deployment Strategies

* The differences can be seen when viewing the deployments in detail using kubectl

## Recreate

* Deletes all the pods running the old version of the application (Scales down to zero) and recreates them with the newer version (Scales back up)
* Not the default deployment strategy
* Causes application downtime

<br>

## Rolling Update

* Replaces the application with the older version with the newer version one pod at a time (Scales down from the old replica set and scales up into the new one, one pod at a time until there's no more pods in the old replica set)
* Allows the upgrade to be seamless and prevent any application downtime
* Allows the user to do a rollback back to the previous version if needed (Scales down from the new replica set and scales up into the old one, one pod at a time until there's no more pods in the new replica set)