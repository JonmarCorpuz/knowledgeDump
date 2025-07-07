# ReplicaSet Overview

* A process that monitors pods 
* Can manage pods that were not created as part of the replica set creation
* The selector needs to be configured under the ReplicaSet spec to match the labels defined in the pod in order to connect the ReplicaSets to the pods (If the labels match upon creation then the ReplicaSet is created successfully)

<br>

# Labels and Selectors

* Used to filter through pods 