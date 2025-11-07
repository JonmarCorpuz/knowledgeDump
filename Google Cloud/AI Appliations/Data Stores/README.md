# Data Store Overview

* A single data store can contain only one type of data
* Each data store has one or more data records (**Document**)

<br>

| Data Store Data Type | Description |
| --- | --- |
| [Website Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#:~:text=type%20of%20data.-,Website%20data,-Structured%20data) uses data indexed from public websites | |
| [Structured Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#structured-data) | |
| [Structured Content](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#structured-data-media) | |
| [Unstructured Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#:~:text=Structured%20content%20(media)-,Unstructured%20data,-Healthcare%20FHIR%20data) | |
| [Healthcare FHIR Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#:~:text=Unstructured%20data-,Healthcare%20FHIR%20data,-Website%20data) | |

<br>

# Data Store Components

## Documents

A document is a data record that's stored in a data store

* Each data stores has one or more 

| Data Store Data Type | Document |
| --- | --- |
| Website Data | Web page |
| Structured Data | A row in a table or a JSON record that follows a particular schema |
| Structured Media | A row in a table or a JSON record that follows a schema that is specific to media |
| Unstructured Data | A file in HTML, a PDF with embedded text, or a file in TXT format |
| Healthcare FHIR Data | A supported FHIR R4 resource |