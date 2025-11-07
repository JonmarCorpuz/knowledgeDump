# VM Instance Migrations Overview

<br>

## Supported Migrations

* Legacy network to a VPC network in the same project
* One VPC network to another VPC network in the same project
* One subnet of a CPV network to another subnet of the same network
* A service project network to the shared network of a Shared VPC host project

<br>

## Migration Limitations

* A VM interface cannot be migrated to a legacy network
* The MAC address allocated to the network interface changes during the migration
* The internal IP address of the VM you're migrating must change if it's being migrated to a network or subnet with a different IP range (The old IP address can be kept only if the new subnet has the same IP range as the subnet that the VM instance is currently in)
* An existing external IP address can be kept when migrating to a new subnet (Specific permissions are required in the target network in order to do this and it must have external IP addresses enabled)

<br>

# VPC Migration

* Must be stopped before it can be migrated
* Must not be part of an instance group of network endpoint group (If part of an unmanaged instance group or network endpoint point, the VM needs to be taken out of that group before migrating it)
* VMs in target pools can be moved without removing them first from their target pool