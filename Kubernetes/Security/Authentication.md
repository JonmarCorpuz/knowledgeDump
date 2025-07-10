# Kubernetes Authentication Overview

* All user access is managed by the kube-apiserver (It authenticates the request before processing it)

<br>

# Authentication Mechanisms

<br>

## Static Files

* Not a recommended authentication mechanism
* Consider volume mount while providing the auth file in a kubeadm setup

### Passwords

* You can use a CSV file to store user details (*password*, *username*, *user ID*) and pass the file using the `--basic-auth-file=FILENAME.csv` flag to the kube-apiserver in the service

<br>

### Tokens

* You can use a CSV file to store user details (*token*, *username*, *user ID*) and pass the file using the `--token-auth-file=FILENAME.csv` flag to the kube-apiserver in the service

<br>

## Certificates

<br>

## Identity Services