# Block Storage Overview

Block storage is used for boot and data volumes for all compute engine instances <sup>[1]</sup> (*VM instances*, *Containers*, *Bare metal instances*, *etc.*) .

* Also known as disks or volumes

## Table of Contents

[Block Storage Types](www.google.com)<br>
|__ [Temporary Block Storage](www.google.com)<br>
|__ [Durable Block Storage](www.google.com)<br>

[References](www.google.com)<br>

# Block Storage Types

## Temporary Block Storage

Temporary block storage <sup>[2]</sup> is a disk that physically attached to the physical host

* Data is lost if the VM is stopped, suspended, or restarted
* Offers the fastest performance among all block storage types
* Used for only scratch data (*Cache*, *etc.*)
* Can't be used as a boot volume

| Temporary Block Storage Solution | Description |
| --- | --- | 
| Local SSD | tmp |

<br>

## Durable Block Storage

Durable block storage <sup>[3]</sup> is a disk that's network-attached to a VM instance

* Used for data that needs to be preserved after a VM turns on and off
* Independent of the compute instances that they're attached to (You can attach and detach them)

| Durable Block Storage | Description |
| --- | --- |
| Hyperdisk | |
| Persistent Disk | |

<br>

# Disks

## Local SSD

Local Solid State Drive <sup>[4]</sup>

* Offers superior IOPS (Higher performance) and low latency compared to durable block storage solutions
* Performance depends on several factors (*Number of attached Local SSD disks - More attached Local SSDs increases performance*, *The selected disk interface - NVMe <sup>[6]</sup> or SCSI <sup>[7]</sup>*, *Instance machine type*, *etc.*)

| Local SSD Type | Description |
| --- | --- |
| Titanium SSD | Custom-designed local SSD that uses Titanium I/O offload processing <sup>[5]</sup> (Titanium SSD performance limits <sup>[8]</sup>) |
| Local SSD | The original local SSD feature (NVMe performance <sup>[9]</sup> and SCSI performance <sup>[10]</sup>) |

<br>

## Hyperdisk

* Data is encrypted at rest and in transit (You can customize the encryption with your own keys)

<br>

## Persistent Disk

* Data is encrypted at rest and in transit (You can customize the encryption with your own keys)

<br>

# References

[1] https://cloud.google.com/compute/docs/disks#:~:text=You%20can%20use%20block%20storage%20for%20boot%20and%20data%20volumes%20for%20all%20compute%20instances%2C%20including%20virtual%20machines%20(VMs)%2C%20containers%2C%20and%20bare%20metal%20instances<br>
[2] https://cloud.google.com/compute/docs/disks#localssds<br>
[3] https://cloud.google.com/compute/docs/disks#temp-vs-durable<br>
[4] https://cloud.google.com/compute/docs/disks/local-ssd<br>
[5] https://cloud.google.com/titanium<br> 
[6] https://cloud.google.com/compute/docs/disks/<br>local-ssd#:~:text=selected%20disk%20interface%20(-,NVMe,-or%20SCSI)%2C%20and
[7] https://cloud.google.com/compute/docs/disks/local-ssd#:~:text=interface%20(NVMe%20or-,SCSI,-)%2C%20and%20the%20instance%27s<br> 
[8] https://cloud.google.com/compute/docs/disks/local-ssd#titanium-ssd-perf-nvme<br>
[9] https://cloud.google.com/compute/docs/disks/local-ssd#local-ssd-perf-nvme<br>
[10] https://cloud.google.com/compute/docs/disks/local-ssd#local-ssd-perf-scsi<br>
