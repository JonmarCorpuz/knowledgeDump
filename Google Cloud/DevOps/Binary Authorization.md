# Binary Authorization Overview

[Binary Authorization](https://cloud.google.com/binary-authorization/docs/overview#what-is-binauthz) is a Google Cloud product that allows you to implement software supply-chain security measures when you develop and deploy container-based applications

* Allows you to periodically monitor the container images associated with running Pods to see if they conform to a policy that you defined through [Continuous Validation with check-based platform policies](https://cloud.google.com/binary-authorization/docs/overview#cv)
* Allows you to enforce policies to ensure that images are being deployed to one of the supported container-based platforms (*GKE*, *Cloud Run*, *Cloud Service Mesh*, *Google Distributed Cloud Software*)
* Allows teams to secure what software is sourced, built, tested, released, and deployed according to internal best practices and standards
* Aims to reduce the risk of deploying defective, vulnerable, or unauthorized software in a container-based environment by preventing images from being deployed unless it satisfies a policy you define

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Image Deployment Lifecycle

1. Build and unit testing
2. Delpoyment into a development environment where users aren't affected
3. Deployment into a QA environment where only internal users are affected
4. Deployment into a canary environment where only a fraction of external users are affected
5. Deployment into production

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Policy Model

Binary Authorization implements a policy model (A policy is a set of rules that governs the deployment of container images and the rules provide specific criteria that an image must satisfy before it can be deployed)
