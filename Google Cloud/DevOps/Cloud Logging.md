# Cloud Logging Overview

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Log Views

A log view is a feature that manages and controls access to log entries

* Allows administrators to define fine-grained access control by specifying filters that determine which log entries can be viewed by particular users, groups, or services

## _Default

The `_Default` log view is configured to include a variety of operational logs that are useful for regular monitoring and troublehsooting tasks but excludes certain types of logs deemed more sensitive

* A predefined log view that's automatically created for each bucket
* Intended to be a practical choice for development teams, operations staff, and other stakeholders who need regular access to operational logs without exposing more sensitive logging information
* Commonly used for day-to-day operations (*Applications monitoring*, *Performance analysis*, *Routing debugging*, *etc.*)
* Helps maintain security and privacy by restricting access to logs that could potentically expose sensitive data or internal operations beyond what is necessary for operational oversight

## _AllLogs

The `_AllLogs` log view is configured to include all log entries stored in the associated log bucket without filtering out any logs based on their content or type (*System activity logs*, *Error logs*, *Audit logs*, *Access Transparency logs*, *Data Access logs*, *etc.*)

* A predefined log view that's automatically created for each bucket
* Offers full access to all log data
* Should only be restricted to users who need complete visibility over all logs

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)
