# Binary Authorization Overview

[Binary Authorization](https://cloud.google.com/binary-authorization/docs/overview) is a deploy-time security control in GKE that ensures that only trusted container images are deployed on your Kubernetes clusters

* Integrates with GKE to enforce container image security policies before allowing the deployment of an image
* Allows you to create and enforce policies and requirements that dictate what images can or cannot be deployed (*Ensuring images are built in a controlled and secure environment*, *Ensure that images pass certain compliance checks before deployment*, *etc.*)
* Uses a concept called attestations, which are verifications that certain conditions have been met before an image is deployed (These attestations are created by authorized entities after the required checks are complete)
* Can be integrated with CI/CD pipelines to automatically check and attest images during the build and deployment process
* Provides an audit trail (*Records decisions regarding image deployments*, *etc.*)
* Helps prevent unauthorized changes or deployments by ensuring only attested images run in your GKE clusters
* Automates the enforcement of security policies
