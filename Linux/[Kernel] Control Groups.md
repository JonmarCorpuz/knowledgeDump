# Control Group Overview

Control Groups are a kernel feature that allows you to group processes together and control their access to system resources (*CPU*, *RAM*, *Disk I/O*, *etc.*)

* Allows you to apply resources limits for a group or processes
* Allows you to prioritize a group of processes before others
* Isolates groups from each other
* Monitors how much memory or CPU a process group uses
* Can temporarily pause and resume groups of processes

<br>

# cgroup Controller

A controller is a kernel component that manages a specific type of system resource for a group of processes

* A container or group that holds processes
* Enforces the rules for a particular resource within that group

<br>

| cgroup Controller | Controlled Resource |
| --- | --- |
| `cpu` | Tracks CPU uage and scheduling |
| `cpuacct` | Tracks CPU time used by processes |
| `cpuset` | Assigns CPUs and memory nodes |
| `memory` | Limits and tracks memory usage |
| `blkio` | Disk Throughput |
| `pids` | Limits the number of processes |
| `freezer` | Freezes and resumes process execution |
| `devices` | Access to device files | 
| `net_cls`/`net_prio` | Network traffic tagging and priority |

<br>

# cgroup Versions

## cgroups v1

*  in `/sys/fs/cgroup/` in most Linux systems

## cgroups v2

