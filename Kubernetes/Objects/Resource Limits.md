# Resource Limits Overview

* A container has no limit to the resources it can consume on a node by default whihc can prevent another pod running on the same node from using resources (No set CPU or memory requests or limits by default)
* A pod will **throttle** the CPU so that it won't go over the specified limit
* A pod can consume more memory than its limit so if it tries to consumer more memory then it'll be terminated with an **OOM** error

<br>

# Limits

<br>

## Limit Ranges

* Applicable at the namespace level
* Only affects newer pods after the limit range is created or updated

<br>

# Requests

<br>

# Resource Limits and Request Strategies

| Request | Limit | Description |
| --- | --- | --- |
| No | No | One pod can consume as much resources it wants from the node which can preventing other pods from being able to use resources on the same node |
| Yes | No | One pod can use as much resources it wants without having to worry about another pod not being given enough resources because each pod is guaranteed the specified amount of resources |
| No | Yes | Each pod is given a limit of how many resources it can consume from a node but doesn't use a node's full capability when the other pods aren't consuming any resources |
| Yes | Yes | |

<br>

# Resource Quotas

A namespace level object that's used to set limits and requests for all objects in the same namespace