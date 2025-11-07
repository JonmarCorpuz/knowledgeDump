# Website Data Overview

[Website Data](https://cloud.google.com/generative-ai-app-builder/docs/create-datastore-ingest#:~:text=type%20of%20data.-,Website%20data,-Structured%20data) uses data indexed from public websites

* Users can provide URL patterns and enable search over the data crawled from the web pages that fit the pattern (*Text*, *Images tagged with metadata*, *etc.*)
* Users can also provide URL patterns for portions of websites that they want to exclude from the data store (Excluded URLs take priority over included ones)

<br>

# Website Data Stores Type

## Basic Website Search

* Provides search capabilities over the existing Google Search index for the included websites
* Doesn't require domain verification

<br>

## Advanced Website Indexing

* Provides advanced search capabilities over an index
* Requires Vertex AI Search data stores owners to verify the domains to which the included websites belong
* Provides that capability to add structured data to the data store schema (A website can contain unstructured data but you can add structured data in the form of `meta` tags, PageMap attributes, and schema.org data to your web pagegs and then use this structured data to edit the data store schemas )

<br>

# Preparing Data for Website Search