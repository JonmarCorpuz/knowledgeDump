# Bigtable Overview

Google's NoSQL big data database service

* Handles massive workloads
* Provides consistent low latency and high throughput
* Used for operational and analytical applications (Ex: *Working with more than 1TB of semi-structured or unstructured data*, *Their data is fast and rapidly changing*, *Data is a time-series or has natural semantic ordering*, *Working with big data that's running asynchronous batch or synchronous real-time processing on the data*, *Running maching learning algorithms on their data*, *etc.*)

<br>

# Bigtable Data Manipulation

## Data Service Layer

* Data can be read from and written to Bigtable through a Data service layer (*Managed VMs*, *HBase REST Server*, *Java Server*, *etc.) using APIs

<br>

## Stream Processing Frameworks

* Data can be streamed into Bigtable using various Stream processing frameworks (*Dataflow*, *Spark Streaming*, *Storm*, *etc.*)

<br>

## Batch Processes

* Data can be read from and written to Bigtable through batch processes (*Hadoop MapReduce*, *Dataflow*, *Spark*, *etc.*)