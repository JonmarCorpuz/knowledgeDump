# Jobs Overview

A job in Jenkins is a specific task (*Compiling code*, *Running tests*, *Deploying code to an environment*, *etc.*)

<br>

# Builds

A build is an execution of a job (Refers to one run of a process that Jenkins performs)

* A history of failed and successful builds are tracked for troubleshooting purposes

<br>

# Jenkins Fingerprints

Jenkins fingerprints are unique hashes that are used to track files (Typically build artifacts) across jobs, builds, and nodes

* Helps trace where a file was created, used, or modified within Jenkins jobs
* Stored on the Jenkins controller's file system under `$JENKINS_HOME/fingerprints/` in a directory based on a partial hash of the file and within it, Jenkins creates an XML file that holds the metadata (*The original file name*, *The MD5 hash*, *A list of jobs and builds that produced or used this artifact*, *Timestamps*, *etc.*)
* Requires all relevant projects to be configured to Record fingerprints of the jar files

<br>

# Parameters

<br>

# References

[1] [Fingerprints](https://www.jenkins.io/doc/book/using/fingerprints/#fingerprints) <br>