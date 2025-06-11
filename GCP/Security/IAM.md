# IAM Overview

* Administrators can apply policies that define **who** (Principal) can do **what** (Role) on which resources

# IAM Components

## Principal

A principal is the entity (*Google account*, *Google group*, *Service account*, *Cloud Identity domain*) that you want to assign a role to

* Each principal has their own identifier

## Role

A role is a collection of permissions that define what actions a principal can perform on GCP resources

| IAM Role Type | Description |
| --- | --- |
| Basic | Too broad |
| Predefined | |
| Custom | Can only be applied to either the project level or organization level |