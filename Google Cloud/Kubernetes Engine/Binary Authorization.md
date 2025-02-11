# Binary Authorization Overview

[Binary Authorization](https://cloud.google.com/binary-authorization/docs/overview) is a deploy-time security control in GKE that ensures that only trusted container images are deployed on your Kubernetes clusters

* Integrates with GKE to enforce container image security policies before allowing the deployment of an image
* Allows you to create and enforce policies and requirements that dictate what images can or cannot be deployed (*Ensuring images are built in a controlled and secure environment*, *Ensure that images pass certain compliance checks before deployment*, *etc.*)
* Checks for the presence of required attestations as part of its enforcement policy (The policy specifies which attestations an image must have before it can be deployed)
* Provides an audit trail (*Records decisions regarding image deployments*, *etc.*)
* Helps prevent unauthorized changes or deployments by ensuring only attested images run in your GKE clusters
* Automates the enforcement of security policies

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Image Attestations

An image attestation is a signed metadata that confirms that an image has met specific conditions or has passed certain tests

* Typically created and signed by an automated process or by truster personnel following the successful completion of a security check or other validation steps
* Created by attesters (Services or individuals authorized to validate and certify that the image has met predefined criteria)
* Images can be automatically scanned and attested during the Continuous Integration and Continuous Deployment process
* Stored in a secure and accessible location
* Helps enforce security best practices and compliance requirements by ensuring that only verified images that meet specific standards are allowed to run (Reduces the risk of deploying images with known vulnerabilities or configuration errors

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)
