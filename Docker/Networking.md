# Docker Networking Overview

* Containers in a Docker network receive a unique IP address, which allows all containers within the same network to communicate with each other
* We can assign names to containers and use them as aliases (This is best since IP addresses may change on container recreation and names are more stable)
* Containers can be connected to multiple networks and will receive a unique IP address per network

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Network Drivers

Network drivers are plugins that provide the underlying networking technology to support network communications between containers and the outside world

* Responsible for the management of network stacks and environments for containers

## Bridge 

The bridge network driver creates a private network on the host machine where your containers can communicate with each other

* Each container connected to the bridge network will receive an internal IP address (Suitable for most single-host scenarios)
* The host can communicate with the containers through NAT
* DNS resolution and auto discovery isn't available in the default bridge network

## Host

The host network driver removes the network isolation between the Docker host and the containers by using the host's networking directly

* Containers using the host network can access all network interfaces of the host (Useful for maximum performance when strict isolation is not required)

## None

The none network driver disables all networking for the containers

* Typically used when you want to completely isolate a container's networking

## Overlay

The overlay network driver is used in Docker Swarm environments to enable containers running on different nodes to communicate with each other

* Essential for creating swarm clusters or distributed applications
* Extends the bridge capabilities across multiple Docker hosts

## Macvlan

The macvlan network driver allows containers to appear as physical devices on the network by giving each container its own MAC address

* Assigning containers a MAC address of their own makes it possible to assign an IP address to each container directly from the network

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)
