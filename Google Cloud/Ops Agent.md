# Ops Agent Overview

The Ops Agent is a monitoring and logging agent designed to collect metrics and logs from VM instances running on Google Cloud

* Helps provide visibility into the performance and health of your application and infrastructure
* A combination of Google's Monitoring Agent and Logging Agent

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Ops Agent Features

| Ops Agent Feature | Description |
| --- | --- |
| Unified Agent | Provides a simplified installation and management experience by collecting both metrics and logs (Reduces the need for managing multiple agents) |
| Metrics Collection | Supports collecting system metrics, application metrics, and custom metrics (The metrics can then be visualized in Google Cloud's operations suite) |
| Log Collection | Automatically collect logs from various common third-party applications and system components (*Apache logs*, *MySQL logs*, *Linux system logs*, *Custom logs*, *etc.*) |
| Customizability | Allows users to specify what metrics and logs to collect |

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Ops Agent Installation



![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Ops Agent Configurations

| Ops Agent Configuration Components | Description |
| --- | --- |
| receiver | Describes the data to collect from log files (This data is mapped into a TIMESTAMP, RECORD model |
| processor | An optional element the describes how the agent can modify the collected information |
| service | Links receivers and processors together to create data flows, called pipelines (Can include multiple pipeline definitions) |

/etc/google-cloud-ops-agent/config.yaml
```YAML
logging:
  receivers:
    syslog:
      type: files
      include_paths:
      - /var/log/messages
      - /var/log/syslog
  service:
    pipelines:
      default_pipeline:
        receivers: [syslog]
metrics:
  receivers:
    hostmetrics:
      type: hostmetrics
      collection_interval: 60s
  processors:
    metrics_filter:
      type: exclude_metrics
      metrics_pattern: []
  service:
    pipelines:
      default_pipeline:
        receivers: [hostmetrics]
        processors: [metrics_filter]
```

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)
