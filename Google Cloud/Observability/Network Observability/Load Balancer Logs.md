# Load Balancer Logs Overview

* The log type and log fields supported vary based on the type of load balancer
* Activated and deactivated on a per backend service basis

<br>

# Load Balancer Log Record Fields

| Load Balancer Log Record Field | Description |
| --- | --- |
| **LogEntry** | Contains severity, project ID, project number, and timestamp information |
| **httpRequest** | Contains a method, URL, status, remote IP address, latency string |
| **resource** | Contains the monitored resource associated with a log entry |
| **jsonPayload** | Contains **statusDetails** field that includes a string that explains why the load balancer returned the HTTP status, cache, and failure information |