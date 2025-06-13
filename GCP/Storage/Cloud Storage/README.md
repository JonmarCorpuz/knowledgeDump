# Cloud Storage Overview

* A durable and highly available object storage solution
* Allows customers to store any amount of data to retrieve it as often as possible
* Primarily used when BLOB (Binary Large-Object) is needed (*Online content*, *Backup and archiving*, *Storage of intermediate results and processing workflows*, *etc.*)

<br>

# Cloud Storage Components

## Object Storage File

* Stored in a packaged format containing the binary form of the actual data itself, the relevant associated metadata, and a globally unique ID
* The unique keys are in the form of URLs
* Storage objects are immutable (A new version of the object is created after every change made)
* Versioning can be enabled (New versions will always override older versions by default)
* ACLs and IAM roles can be used to restrict who has access to certain buckets

## Bucket

* Requires a specified unique ID and a geographic location for where it should be stored 