# Apply Overview

* Takes into consideration the local configuration file, the live object definition on Kubernetes, and the last applied configuration before making a decision on what changes are made
* The object is created if it doesn't already exist when the kubctl apply command is run
* The YAML version of the local object configuration is converted into a JSON format and then stored as the last applied configuration
* The YAML file, JSON file, and live object configuration file are compared to identify what changes are to be made on the live object (The live object configuration file is updated if there are any differences)
* The YAML file is the source of truth and both the live object configuration file and the JSON file will try to match that
* The live object configuration is stored in the Kubernetes memory (The JSON file is stored on the live object configuration file on the Kubernetes cluster as an annotation named "last-applied-configuration" and is stored here only when using the kubectl apply command)
