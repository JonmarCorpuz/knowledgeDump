# CloudWatch Agent Overview

The CloudWatch agent is a software component that collects metrics, logs, and traces from your EC2 instances, on-premises servers, and containerized applications

* Enables users to monitor their infrastructure and applications more comprehensiveley than the basic monitoring providing by default

<br>

# CloudWatch Agent Benefits

* Collects system-level metrics (*CPU*, *Memory*, *Disk*, *Network*)
* Gathers customer metrics from your applications
* Collects and centralizes logs from various sources
* Monitors both AWS and on-premises environments with a single tool
* Sets up alarms and notifications based on collected data

<br>

# CloudWatch Agent Features

* Collects internal system-metrics from EC2 instances across operation systems
* Collects system-level metrics from on-premises servers
* Retrieves custom metrics from your applications or services using the `StatsD` and `collectd` protocols

<br>

# Install CloudWatch Agent

```Bash
cd /tmp
wget https://s3.amazonaws.com/amazoncloudwatch-agent/ubuntu/amd64/latest/amazon-cloudwatch-agent.deb
sudo dpkg -i amazon-cloudwatch-agent.deb
```

