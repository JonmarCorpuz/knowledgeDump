# Pipeline Overview

* Resilient by design (*Can survive unexpected restarts of the Jenkins controller*, *etc.*)
* Can be paused at specific points allowing for manual intervention or approval before continuing the build process
* Promotes efficient build management by reducing the number of jobs needed compared to the Freestyle projects (*They can define stages with multiple steps within a single pipeline job*, *etc.*)

<br>

# Pipeline Categories

* Both categories are denoted as a Jenkinsfile and make use of the same pipeline subsystem
* Both relies on the Apache Groovy syntax

## Declarative Pipelines

* Offers a simpler human-readable format to define the pipeline
* Not suitable for highlt complex workflows that require extensive scripting for conditional logic or custom actions

## Scripted Pipelines

* Offers the most control and flexibility
* Requires a complete Groovy script Jenkinsfile to define all stages and steps of your workflow
* Ideal for highly complex workflows for precise control and customization

<br>

# Jenkinsfile

A Jenkinsfile is a text file that defines the build pipeline for a Jenkins project using code (Tells Jenkins what steps to follow to build, test, and deploy your projects)

* Written in Groovy-based syntax and checked into your project's source control (*Git*, *etc.*)

```Groovy
pipeline {
    agent any

    stages {
        stage(){
            agent { }
            steps {
                echo "test"ls
                git add
            }
        }
    }
}
```

## Stages

A stage is the main section of a pipeline that define the high-level stops of your build, test, and deploy process

* Allow parallel task execution
* Configured via the Jenkinsfile

<br>

# References

[1] [Using a Jenkinsfile](https://www.jenkins.io/doc/book/pipeline/jenkinsfile/#using-a-jenkinsfile) <br>