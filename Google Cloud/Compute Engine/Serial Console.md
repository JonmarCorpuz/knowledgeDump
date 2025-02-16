# Serial Console Overview

A serial console is a low-level interface that allows you to interact with a computer or other device directly

* Bypasses network and software dependencies that might be unavailable or non-functional in certain situations (*During system boot*, *If the device's network configuration is incorrect*, *etc.*)
* Provides text-based access to a device through a serial communication interface (*Physical port*, *Virtualized interface*, *etc.*)
* Primarily used for troubleshooting and managing systems when they become unresponsive or isolated from the network
* Allows you to access the BIOS/UEFI settings, boot loader, OS boot messages, and system command prompt of a VM instance
* Helps diagnose issues occuring at boot time by having all messages and outputs directed to the serial console during the boot process

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Serial Port

A serial port is a type of interface on a device that enables serial communication where data is transmitted one bit at a time over a communication channel or computer bus

* Allows devices to send and receive data asynchronously without the need for the sending and receiving clocks to be synchronized by transmitting data in a sequence of bits
* Generally requires fewer wires and can achieve longer transmission distances compared to parallel ports (Interfaces between two devices where data is transferred simultaneously across multiple wires or channels)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Serial Console Logs

Serial console logs are records of all data that passes through a VM's serial console (*System messages*, *Login sessions*, *Configuration changes*, *Debug information*, *etc.*)

* Can be viewed using the console or with the `gcloud compute instances get-serial-port-output VM_NAME --zone ZONE` command
* Can be crucial for understanding the behavior of a system before a failure or during unexpected behavior
* Commonly used in environments where critical systems must be available at all times (*Data centers*, *Telecommunications*, *Industrial control systems*, *etc.*)
