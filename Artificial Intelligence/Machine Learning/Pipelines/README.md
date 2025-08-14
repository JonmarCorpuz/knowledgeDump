# Machine Learning Pipelines Overview

A [machine learning pipeline](https://cloud.google.com/vertex-ai/docs/pipelines/introduction#ml-pipeline) is a portable and extensible description of an MLOps workflow as a series of steps (Pipeline tasks)

* Each pipeline task performs a specific step in the workflow to train  and deploy an ML model
* Allows users to apply MLOps strategies to automate and monitor repeatable processes in their ML practice (Ex: *Reuse a pipeline definition to continuously retrain a model on the latest production data*)

<br>

# Pipeline Tasks

A [pipeline task](https://cloud.google.com/vertex-ai/docs/pipelines/introduction#pipeline-task) is the instantiation of a pipeline component that performs a specific step in your ML workflow

* Each pipeline task can be created either in Python or as a prebuilt container image
* An ML pipeline is a DAG (Directed Acyclic Graph) of containerized pipeline tasks that are interconnected using input-output dependencies
* Each can be defined as a DAG using either the Kubeflow Pipelines SDK or the TFX SDK, compile it to its YAML for intermediate representation, and then run the pipeline
* Runs tasks in parallel by default and each can be linked together to execute them in series

<br>

