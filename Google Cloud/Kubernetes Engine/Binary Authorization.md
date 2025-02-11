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

# Binary Authorization Configuration

```YAML
apiVersion: binaryauthorization.googleapis.com/v1
kind: Policy
metadata:
  name: "projects/my-project-id/policy"
defaultAdmissionRule:
  evaluationMode: REQUIRE_ATTESTATION
  enforcementMode: ENFORCED_BLOCK_AND_AUDIT_LOG
  requireAttestationsBy:
    - projects/my-project-id/attestors/my-attestor
admissionWhitelistPatterns:
  - namePattern: "gcr.io/my-project-id/whitelisted-image:*"
clusterAdmissionRules:
  "us-central1-a.my-cluster":
    evaluationMode: REQUIRE_ATTESTATION
    enforcementMode: ENFORCED_BLOCK_AND_AUDIT_LOG
    requireAttestationsBy:
      - projects/my-project-id/attestors/my-attestor
globalPolicyEvaluationMode: ENABLE
```

* `apiVersion` specifies the API version for Binary Authorization
* `kind` identifies the resource type
* `metadata` provides metadata about the resource
* `defaultAdmissionRule` defines the default policy for all clusters in the project unless overridden by specific cluster adminssion rules
* `admissionWhitelistPatterns` specifies which container images are allowed without attestation
* `clusterAdmissionRules` allows for specifying admission rules that apply to specific clusters
* `globalPolicyEvaluationMode` allows the policy to be enforced globally across all clusters if enabled

## Whitelist Name Pattern

A whitelist name pattern (`admissionWhitelistPatterns`) refers to a specified pattern or set of rules used to identify container images that are allowed to be deployed on your Kubernetes cluster without requiring attestation

* Allows users to control which container images can run based on their registry path, repository name, or tag and digests
* Helps ensure that only authorized images from certain registries and repositories or with specific tags are permitted to be deployed
