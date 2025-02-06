# Secret Manager Overview

[Secret Manager](https://cloud.google.com/secret-manager/docs/overview) is a secrets and credentials management service that elts you store and manage sensitive data (*API keys*, *Usernames*, *Passwords*, *Certificates*, *etc.*)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Secrets Availability

## Mounting Secrets

* You can mount a secret as a volume to a resource in order to make it available as a file
* Reading a volume always fetches value from Secret Manager so that the resource has access to the latest version of the secret directly from Secret Manager

## Passing Secrets

* You can pass a secret using environment variables
