# Workload Overview

A workload is a collection of applications and their configurations that you want to run on your Kubernetes cluster

* Primarily managed through workload resources that specifies how applications should run and interact within the Kubernetes environment

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Workload Resources

## Pods

A Pod represents a single instance of a running process in your cluster and consists of containers or a small group of containers that share resources

* Managed by a single entity
* The smallest and most basic deployable Kubernetes object
* The containers inside a Pod share the same network space (*IP address*, *Port space*, *etc.*) and storage, which are mounted as volumes
* Containers in the same Pod can communicate with each other using standard inter-process communications (*SystemV semaphores*, *POSIX shared memory*)
* Can specify a set of shared storage volumes that can be shared among the containers

## Deployments

A Deployment describes how replicas of software should be created and managed

* Manages stateless applications
* Provides declarative updates to applications
* Used to control the creation, scaling, and updating of Pods
* Can manage the rollout of updates to your application and can rollback to a previous version of the application if something goes wrong
* Automatically restarts Pods that fail, are evicted, or are terminated in order to ensure that the desired state of the system matches the observed state

| Deployment Component | Description |
| --- | --- |
| Pod Template | A template that describes the Pod that'll be created (*What container images to use*, *Ports to expose*, *Environment variables*, *etc.*) |
| Replica Count | The number of replicas that should be running in the cluster |
| Selector | Labels that determine which Pods are managed by the Deployment (Ensures that the Deployment manages only the Pods that match its selector |
| Strategy | Defines the strategy used to replace old Pods with new ones (*Rolling update*, *Recreate*, *etc.*) |

## StatefulSets

A StatefulSet is a workload API object that manages stateful applications

* Manages the deployment and scaling of a set of Pods
* Provides guarantees about the ordering and uniqueness of Pods
* Suitable for applications that require stable and persistent storage, unique network identifiers, and graceful deployment and scaling

## DaemonSets

A DaemonSet is a workload API object that manages the deployment of a copy of a Pod on certain or all Nodes in a Kubernetes cluster

* Ensures that as Nodes are added to the cluster, Pods are added to them accordingly (Similarly, as Nodes are removed, those Pods are garbage collected)
* Ensures that every Node in the cluster runs a copy of a specified Pod (Useful for deploying infrastructure-related tasks that need to be run on all or some specific Nodes)

## Jobs

A Job is a workload resource that manages a process or a set of processes that need to run to completion (*Batch procecssing*, *Scheduled tasks*, *etc.*)

* Designed to execute a process that performs a specific task and then terminates
* Creates one or more Pods to run the Job
* Can be configured to run multiple Pods in parallel in order to allow batch processing and parallel processing to significantly reduce the time required to complete tasks that can be parallelized
* Kubernetes can automatically retry Pods that fail during a Job execution, ensuring that the Job eventually completes if possible

## CronJobs

A CronJob manages time-based Jobs by scheduling them at specified times, dates, or intervals

* Uses the Unix cron string format
* Kubernetes ensures that the Jobs complete successfully, and can retry Jobs or skip them if they fail or if the next scheduled time is due
* Supports policies to determine what to do if a Job fails or if too many Jobs are running at once (*Concurrency policies*, *Deadlines*, *etc.*)

| CronJob Policy | Description |
| --- | --- |
| Allow | Allows CronJobs to run concurrently |
| Forbid | Prevents concurrent runs (If a run is attempted while another is still ongoing, it'll skip the new run) |
| Replace | Cancels the currently running job and replcaes it with a new one |
