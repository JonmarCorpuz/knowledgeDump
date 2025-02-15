# Bastion Host Overview

A bastion host is a specially configured VM that's used as a secure and controlled entry point for administrators to connect to other instances or services within a private network

* Usually exposed to the public internet and is highly secured because it's a critical component in managing the security of an infrastructure
* Placed in its own network within its own subnet in order to minimize exposure of the rest of the infrastructure to the public internet
* Hardened with strict security policies to ensure that only authorized users and necessary connections are allowed (*Firewall*, *Access control*, *etc.*)
* Logging and monitoring are enabled to keep track of all activities performed through the bastion host in order to help detect and respond to potential security threats

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Use a Bastion Host

1. Create a bastion host VM using the **gcloud compute instances create VM_NAME --zone=ZONE --machine-type=e2-micro --image-family=IMAGE_FAMILY --image-project=IMAGE_PROJECT --network-interface=subnet=SUBNET,address=""** command
2. Connect to the bastion host using the **gcloud compute ssh BASTION_VM_NAME** command
3. Connect to the main VM through its internal IP address from the bastion host using the **gcloud compute ssh VM_NAME --internal-ip** command

