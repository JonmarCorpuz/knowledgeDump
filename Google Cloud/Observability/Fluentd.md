# Fluentd Overview

Fluentd is a open source tool used for collecting, processing, and forwarding log and event data from various sources to different destinations 

* Fully managed on Google Cloud and serves as a data collector and log forwarding solution
* Ensures that logs from Google Cloud services, applications, and other resources are properly handled and routed to storage or analysis systems

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Fluentd Pipeline

## Input

The input stage (Collecting data) is where Fluentd collects logs from various sources

```Text
# Input: Collect logs from a file
<source>
  @type tail
  path /var/log/app/*.log
  pos_file /var/log/fluentd.pos
  tag app.logs
  format json
</source>
```

## Filter

The filter stage is where you can apply filter plugins to process or transform the data collected (This stage is optional)

```Text
# Filter: Add a new field (e.g., processing timestamp)
<filter app.logs>
  @type record_transformer
  enable_ruby
  <record>
    processed_time ${time.now}
  </record>
</filter>
```

* Allows you to modify the log data (*Changing field names*, *Adding new fields*, *Parsing structured data*, *etc.*)
* Allows you to filter unwanted logs by discarding them based on certain conditions
* Allows you to transform data (*Modify fields*, *Parse JSON*, *Regex subsitution*, *Enrich data with additional context*

## Output

The output stage is where Fluentd sends the processed logs to a destination (*Cloud services*, *Third-party tools*, *Storage systems*, *etc.*)

```Text
# Output: Send the processed logs to Google Cloud Logging
<match app.logs>
  @type google_cloud
  project_id your-project-id
  keyfile /path/to/your-service-account-key.json
  log_name your-log-name
</match>
```

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Fluentd Filter Plugins

## record_transformer

## grep

## geoip

## parses

## filter-record-transformer

The filter-record-transformer is a plugin used to modify or transform log data by adding, changing, or removing fields in the log records

```Text
<filter **>
  @type record_transformer
  enable_ruby
  <record>
    # Add a new field `processed_time` to the log
    processed_time ${Time.now.to_s}
    
    # Change the value of the `status` field (e.g., to `success` if it’s '200')
    status ${record["status"] == "200" ? "success" : "error"}
    
    # Add a custom field based on another field
    request_duration ${record["end_time"] - record["start_time"]}
    
    # Remove sensitive information (e.g., user_id)
    remove_field user_id
  </record>
</filter>
```

* Customized logs as they pass through the Fluentd pipeline
* Allows you to modify or enrich log records based on certain conditions or rules (*Tranforming field values*, *etc.*) in order to filter out unwanted records or adding new fields to the logs
