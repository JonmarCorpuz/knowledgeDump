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

## Default Admission Rule

A default admission rule (`defaultAdmissionRule`) specifies the baseline policy for all container image deployments in a Kubernetes cluster (Unless overridden by more specific rules targeted at particular clusters or namespaces)

* Serves as the fallback policy that applies when no other specific rules match a container image deployment attempt (Ensures that every deployment is checked against a set of predefined criteria unless explicitly configured otherwise)
* Crucial for enforcing security and compliance across all Kubernetes deployments by default (Ensures that any deployment that doesn't meet specific criteria or is not covered by more targeted rules is either allowed, denied, or allowed with logging based on the policy's baseline requirements)

### Evaluation Mode

The evaluation mode (`evaluationMode`) defines how the policy evaluates an image before admissions

* `ALWAYS_ALLOW` indicates that the images are always allowed without any checks
* `ALWAYS_DENY` indicates that the images are always denied
* `REQUIRE_ATTESTATION` indicates that the images must have specific attestations to be admitted
* `SKIP` indicates that no Binary Authorization checks are applied

### Enforcement Mode

THe enforcement mode (`enforcementMode`) specifies how the policy is enforced if the requirements set by the evaluation mode are not met

* `ENFORCED_BLOCK_AND_AUDIT` indicates that the deployment will be blocked and the attempt will be logged
* `DRYRUN_AUDIT_LOG_ONLY` indicates that the deployment will be allowed but will be logged for auditing puposes (Useful for simulating what would happen if it were enforced)
* `DRYRUN_ALLOW_LOG_ONLY` indicates that the action will be logged but doesn't enforce blocks (Useful for testing policy impact without affecting production)

### Require Attestation 

The require attestation (`RequireAttestationBy`) lists the attestors whose attestations are required for the deployment of an image under the REQUIRE_ATTESTATION mode

```YAML
defaultAdmissionRule:
  requireAttestationsBy:
    - projects/my-project-id/attestors/example-attestor
```

## Whitelist Name Pattern

A whitelist name pattern (`admissionWhitelistPatterns`) refers to a specified pattern or set of rules used to identify container images that are allowed to be deployed on your Kubernetes cluster without requiring attestation

* Allows users to control which container images can run based on their registry path, repository name, or tag and digests
* Helps ensure that only authorized images from certain registries and repositories or with specific tags are permitted to be deployed

```YAML
defaultAdmissionRule:
  admissionWhitelistPatterns:
    - namePattern: "VALUE"
    - namePattern: "VALUE"
```
