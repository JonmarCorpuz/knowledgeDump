# Span Overview

A span is a record representing a single operation or unit of work

* Each span captures the start and end time of an operation, its name, and other metadata that describe the operation in more detail

<br>

# Events

An event is a message attached to a span that represents some activity or occurence during the span's lifetime

* Provides additional context within a span
* Can be used to record significant moments or actions within the operation being traced (*When a specific function is called*, *When a database query starts or ends*, *When an error occurs*, *etc.*)

<br>

# Span Filters

Span filters are tools that allow you to narrow down and display only the spans that match specific criteria within your trace data

| Span Filter | Description |
| --- | --- |