# Machine Learning Pipeline Lifecycle Overview

<br>

# Machine Learning Pipeline Lifecycle

## 1. Define

The process of defining and building an ML pipeline

* Choose an ML framework 
* Define pipeline tasks 
* Configure a pipeline

<br>

## 2. Compile

The process of generating the ML pipeline definition in a compiled YAML file or an intermediate representation that can be used to run your ML pipeline

* You can optionally upload the compiled YAML file as a pipeline template to a repository and reuse it to create ML pipeline runs

<br>

## 3. Run

The process of creating an execution instance of your ML pipeline using the compiled YAML file or a pipeline template (Pipeline run)

<br>

## 4, Monitor, Visualize, and Analyze Runs

The process of monitoring the performance and costs of your pipeline runs

* Configure email notifications for pipeline failures
* Use Cloud Logging to create log entries for monitoring events
* Use Cloud Billing export to BigQuery to analyze pipeline run costs

<br>

## 5 Stop or Delete Pipeline Runs (Optional)

Optionally stop a pipeline run, pause it, resume it, or delete it