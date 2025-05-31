# Block Storage Overview

Block storage is used for boot and data volumes for all compute engine instances (*VM instances*, *Containers*, *Bare metal instances*, *etc.*) [1].

* Also known as disks or volumes

## Table of Contents

[Block Storage Types](www.google.com)
|__ [Temporary Block Storage](www.google.com)
|__ [Durable Block Storage](www.google.com)

[References](www.google.com)

# Block Storage Types

## Temporary Block Storage

* Data is lost if the VM is stopped, suspended, or restarted
* Offers the fastest performance among all block storage types
* Used for only scratch data (*Cache*, *etc.*)
* Can't be used as a boot volume

| Temporary Block Storage Solution | Description |
| --- | --- | 
| Local SSD |

## Durable Block Storage



# References

[1] https://cloud.google.com/compute/docs/disks#:~:text=You%20can%20use%20block%20storage%20for%20boot%20and%20data%20volumes%20for%20all%20compute%20instances%2C%20including%20virtual%20machines%20(VMs)%2C%20containers%2C%20and%20bare%20metal%20instances 