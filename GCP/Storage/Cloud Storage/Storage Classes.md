# Storage Class Overview

* No minimum fee (You pay only for what you use)
* Encrypts data on the server side and uses HTTPS/TLS

<br>

# Storage Classes

```Text
Cloud Storage Class
|__ Standard
|__ Nearline
|__ Coldline
|__ Archive
``` 

* All storage classes have unlimited storage (No minimum object size required)
* Worldwide accessibility and locations
* Provides low latency and high durability
* Provides geo-redundancy if data is stored in a multi-region or dual-region
* Provides an **autoclass** feature that automatically transitions objects to appropriate storage classes based on each object's access pattern to simplify cost savings (*Moves data that's not accessed to colder storage classes to reduce storage cost*, *Moves data that's accesed to Standard storage to optimize future accesses*, *etc*)

## Standard

* For hot data

## Nearline

* For data that's accessed once per month

## Coldline

* For data that's accessed once every 90 days

## Archive

* For data that's accessed once a year

<br>

# Cloud Storage Upload Methods

## Online Transfer

## Storage Transfer Service

## Transfer Appliance