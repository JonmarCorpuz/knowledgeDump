# Docker Daemon Overview

`dockerd` is a background service that runs on the host machine and manages the Docker containers on the system by communicating with other Docker tools (*Docker client*, *Docker API*, *etc.*) in order to perform tasks

* In typical use, users interact with the Docker daemon via the Docker client by running Docker commands, which the client will then forward to the daemon to execute
* The core component that handles a wide range of Docker functionalities (*Building Docker containers*, *Distributing Docker containers*, *Running Docker containers*, *etc.*)
* Manages Docker containers (Creates, runs, stops, and manages the states of Docker containers)
* Manages Docker iamges (Can build images from a Dockerfile, pull them from a Docker registry, and manage them on the local system)
* Manages Docker's network bridges, IP addresses, and other networking resources (Allows Docker containers to communicate with each other and the outside world by configuring their network settings)
* Manages Docker volumes
* Can manage services for Docker setups using swarm mode

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

