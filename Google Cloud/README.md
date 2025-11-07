# GCP Overview

<br>

# Storage

Data storage
```Text
|--> Unstructured --> Cloud Storage
|
|--> Structured |---> Type 1: Transactional Workloads |---> SQL -----> Cloud SQL
                |                                     |---> NoSQL ---> Firestore
                |
                |---> Type 2: Analytical Worklaods |------> SQL -----> BigQuery
                                                   |------> NoSQL ---> BigTable
```

<br>

# AI/ML

## Data-to-AI Workflow

| Data-to-AI Workflow Step | Description |
| --- | --- |
| 1. Ingestion and process | Gather data from multiple sources |
| 2. Storage | Save data in different types of storage |
| 3. Analytics | Analyze the data and visualize the results |
| 4. Training | Train a machine learning model to predict future trends or generate new content |

Data-to-AI workflow
```Text
1. Ingestion |---> Pub/Sub
             |---> Dataflow
             |---> Dataproc
             |---> Cloud Data Fusion

2. Storage |-----> Cloud Storage
           |-----> BigQuery
           |-----> Cloud SQL
           |-----> Spanner
           |-----> BigTable
           |-----> Firestore

3. Analytics |---> BigQuery
             |---> Looker

4. Training |----> Vertex AI 
```

<br>

