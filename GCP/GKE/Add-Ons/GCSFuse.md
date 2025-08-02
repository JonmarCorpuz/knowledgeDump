# Google Cloud Storage Fuse CSI Driver Overview

The [GCSFuse CSI](https://cloud.google.com/storage/docs/cloud-storage-fuse/overview#overview) driver allows users to transparently expose buckets as locally mounted folders on their file system

* Works by translating object storage names into a directory-like structure (Interpretates the `/` in object names as a directory separator)
* Objects with the same common prefix are treated as files in the same directory (Objects can be organized into a logical file system structure using a [hierarchical namespace](https://cloud.google.com/storage/docs/hns-overview))