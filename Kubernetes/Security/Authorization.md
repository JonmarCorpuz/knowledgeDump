# Kubernetes Authorization Overview

<br>

# Authorization Mechanisms

## Built-in Mechanisms

### Node Authorizer

* The kubelet reaches out to the kube-apiserver to read information about the cluster (*Services*, *Endpoints*, *Nodes*, *Pods*, *etc.*) and write information about the node (*Node status*, *Pod status*, *Events*, *etc.*)

### Atrribute Based Access Control

### Role Based Access Control



<br>

## Webhook

### Open Policy Agent

<br>

# Authorization Modes

* Set using the `--authorization-mode=AUTHORIZATION_MODE` flag in the kube-apiserver (If not specified, the authorization mode is set to AlwaysAllow by default)
* Multiple authorization modes can be configured and will be used in the order that they're specified (The request moves down the chain each time it's denied and stops going down as soon as a mechanism approves it)

## AlwaysAllow

<br>

## AlwaysDeny