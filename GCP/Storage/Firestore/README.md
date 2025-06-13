# Firestore Overview

* A flexible and horizontally scalable NoSQL cloud database for mobile, web, and server development
* Data is stored in documents and then organized into collections
* Uses NoSQL queries to retrieve individual specific documents or all documents within a collection
* Uses data synchronization to update data in any connected device 
* Designed to make simple one-time fetch queries efficiently
* Caches data that an application is actively using so that it can write, read, listen to, and query data even if the device is offline (When the device comes back online, Firestore synchronizes any local changes back to Firestore)
* Provides automiatc multi-region data replication, strong consistency guarantees, atomic batch operations, and real transaction support

<br>

# Firestore Components

## Documents

* Can contain complex nested objects in addition to subcollections
* Indexed by default (Query performance is proportionate to the size of the result set and not the data set)

## Collections


