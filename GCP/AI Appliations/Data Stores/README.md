# Data Store Overview

* A single data store can contain only one type of data (*Website data*, *Structured data*, *Structured content*, *Unstructured data*, *Healthcare FHIR data*, *etc.*)

<br>

# Data Store Data Types

## Website Data

[Website Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#:~:text=type%20of%20data.-,Website%20data,-Structured%20data) uses data indexed from public websites

* Users can provide URL patterns and enable search over the data crawled from the web pages that fit the pattern (*Text*, *Images tagged with metadata*, *etc.*)
* Users can also provide URL patterns for portions of websites that they want to exclude from the data store (Excluded URLs take priority over included ones)

### Basic Website Search

* Provides search capabilities over the existing Google Search index for the included websites
* Doesn't require domain verification

### Advanced Website Indexing

* Provides advanced search capabilities over an index
* Requires Vertex AI Search data stores owners to verify the domains to which the included websites belong
* Provides that capability to add structured data to the data store schema (A website can contain unstructured data but you can add structured data in the form of `meta` tags, PageMap attributes, and schema.org data to your web pagegs and then use this structured data to edit the data store schemas )

<br>

## Structured Data

[Structured Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#structured-data)

* Enables semantic search or recommendations over structured data
* This type of data can be imported from BigQuery or Cloud Storage (Structured JSON data can also be manually uploaded through the API)

<br>

## Structured Content

[Structured Content](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#structured-data-media)

* Can only be connected to media apps and vice-versa

<br>

## Unstructured Data

[Unstructured Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#:~:text=Structured%20content%20(media)-,Unstructured%20data,-Healthcare%20FHIR%20data)

* Enables semantic search over data (*Documents*, *Images*, *etc.*)
* Supports various document types (*HTML*, *PDF with embedded text*, *TXT*, *PPTX*, *DOCX*, *etc.*)

<br>

## Healthcare FHIR Data

[Healthcare FHIR Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#:~:text=Unstructured%20data-,Healthcare%20FHIR%20data,-Website%20data) 

* Healthcare search apps use GHIR R4 data imported from a Cloud Healthcare API FHIR store