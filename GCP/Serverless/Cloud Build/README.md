# Cloud Build Overview

Cloud Build is a fully managed CI/CD service that allows users to automate the building, testing, and deployment of their application across multiple environments

<br>

# Cloud Build Workflow

## Step 1: Upload or Push Source Code

* Source code can be pulled from **Cloud Source Repositories**, **GitHub**, **BitBucket**, and **Cloud Storage**
* Code pushes can automatically trigger a build via **Cloud Build Trigger** if configured

## Step 2 (Optional): Configure Trigger

* Can specify to start the build on **push to branch**, **pull request**, **tag**, or **manual invocation**
* Linked to a Cloud Build configuration file or a Dockerfile

## Step 3: Configure Build Configuration File

* Each step runs in a Docker container

## Step 4: Execution of Build Steps

* Spins up virtual environments 
* Runs each step in order
* Handles parallelizaton if defined
* Streams logs in real time

## Step 5 (Optional): Store Artifacts

* Push Docker images to Artifact Registry
* Store files in Cloud Storage
* Send reports to Cloud Logging
* Notify via Pub/Sub, Slack, or email

## Step 6 (Optional): Deploy Application

* Can automatically deploy an application to Cloud Run, App Engine, GKE, Firebase Hosting, or any custom target (*via SSH*, *Terraform*, *etc.*)