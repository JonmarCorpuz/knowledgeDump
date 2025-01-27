# Policy Controller Overview

The Policy Controller is used to enforce policies and ensure compliance across Kubernetes clusters

* Part of the Anthos Config Management toolset
* Designed to help organizations automate the enforcement and auditing of their security, operations, and compliance requirements in Kubernetes environments (Ex: *RBAC*, *Security contexts*, *etc.*)
* Enables you to manage policies as code by using Kubernetes custom resource definitions
* Continuously audits existing clusters to ensure they remain compliant with the policies you're defined (If it detects any discrepancies, it can report them or even bring the resource into compliance automatically depending on the configuration)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Open Policy Agent 

* Policy Controller is built on top of Open Policy Agent Gatekeeper (An open-source policy enforcement project)
* Provides a robust, declarative language for specifying rules and a mechanism to enforce these rules at runtime
