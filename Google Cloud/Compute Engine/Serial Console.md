# Serial Console Overview

A serial console is an interface that allows you to interact with a computer or other device directly at a very low level

* Bypasses network and software dependencies that might be unavailable or non-functional in certain situations (*During system boot*, *If the device's network configuration is incorrect*, *etc.*)
* Provides text-based access to a device through a serial communication interface (*Physical port*, *Virtualized interface*, *etc.*)
* Primarily used for troubleshooting and managing systems when they become unresponsive or isolated from the network
* Allows you to access the BIOS/UEFI settings, boot loader, OS boot messages, and system command prompt of a VM instance
* Helps diagnose issues occuring at boot time by having all messages and outputs directed to the serial console during the boot process

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Serial Console Logs

Serial console logs are records of all data that passes through a VM's serial console

* Can be viewed using the console or with the `gcloud compute instances get-serial-port-output VM_NAME --zone ZONE` command
