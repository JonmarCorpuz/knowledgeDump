# tmp

```Bash
dial up... ERROR dial tcp 127.0.0.1:5044: connect: connection refused
```

<br>

```Bash
$ sudo lsof -i :5044
$
```

<br>

```Bash
[ERROR][elasticsearch-service] Unable to retrieve version information from Elasticsearch nodes. connect ECONNREFUSED 127.0.0.1:9200
[ERROR][elasticsearch-service] Unable to retrieve version information from Elasticsearch nodes. security_exception
```

<br>

```Bash
Could not create auto-configuration directory
```

<br>

# Systemctl Logs

```Bash
Registering task [endpoint:complete-external-response-actions] with timeout of [5m] and run interval of [60s]
```

<br>

```Bash
ExecStart=/usr/share/filebeat/bin/filebeat --environment systemd $BEAT_LOG_OPTS $BEAT_CONFIG_OPTS $BEAT_PATH_OPTS (code=exited, status=2)
```

<br>

# Filebeat

```Bash
Exiting: error unpacking config data: more than one namespace configured accessing 'output' (source:'/etc/filebeat/filebeat.yml')
```

<br>

```Bash
systemd[1]: Failed to start Filebeat sends log files to Logstash or directly to Elasticsearch..
```

<br>

# tmp

**Error**:
```JSON
[2025-06-10T04:27:43,860][ERROR][logstash.filters.geoip   ] Invalid setting for geoip filter plugin:

  filter {
    geoip {
      # This setting must be a path
      # File does not exist or cannot be opened /opt/logstash/vendor/geoip/GeoLite2-City.mmdb
      database => "/opt/logstash/vendor/geoip/GeoLite2-City.mmdb"
      ...
    }
  }
[2025-06-10T04:27:43,865][FATAL][logstash.runner          ] The given configuration is invalid. Reason: Unable to configure plugins: (ConfigurationError) Something is wrong with your configuration.
[2025-06-10T04:27:43,868][FATAL][org.logstash.Logstash    ] Logstash stopped processing because of an error: (SystemExit) exit
org.jruby.exceptions.SystemExit: (SystemExit) exit
        at org.jruby.RubyKernel.exit(org/jruby/RubyKernel.java:924) ~[jruby.jar:?]
        at org.jruby.RubyKernel.exit(org/jruby/RubyKernel.java:883) ~[jruby.jar:?]
        at usr.share.logstash.lib.bootstrap.environment.<main>(/usr/share/logstash/lib/bootstrap/environment.rb:90) ~[?:?]
```

<br>

**Error**:
```JSON
[2025-06-10T04:26:55,977][FATAL][logstash.runner          ] An unexpected error occurred! {:error=>#<RuntimeError: Logstash cannot be run as superuser.>, :backtrace=>["/usr/share/logstash/logstash-core/lib/logstash/runner.rb:430:in running_as_superuser'", "/usr/share/logstash/logstash-core/lib/logstash/runner.rb:259:in execute'", "/usr/share/logstash/vendor/bundle/jruby/3.1.0/gems/clamp-1.3.2/lib/clamp/command.rb:66:in run'", "/usr/share/logstash/logstash-core/lib/logstash/runner.rb:249:in run'", "/usr/share/logstash/vendor/bundle/jruby/3.1.0/gems/clamp-1.3.2/lib/clamp/command.rb:140:in run'", "/usr/share/logstash/lib/bootstrap/environment.rb:89:in <main>'"]}
[2025-06-10T04:26:55,984][FATAL][org.logstash.Logstash    ] Logstash stopped processing because of an error: (SystemExit) exit
org.jruby.exceptions.SystemExit: (SystemExit) exit
        at org.jruby.RubyKernel.exit(org/jruby/RubyKernel.java:924) ~[jruby.jar:?]
        at org.jruby.RubyKernel.exit(org/jruby/RubyKernel.java:883) ~[jruby.jar:?]
        at usr.share.logstash.lib.bootstrap.environment.<main>(/usr/share/logstash/lib/bootstrap/environment.rb:90) ~[?:?]
```

<br>

```JSON
Caused by: org.apache.lucene.index.IndexFormatTooOldException: Format version is not supported (resource BufferedChecksumIndexInput(NIOFSIndexInput(path="/var/lib/elasticsearch/nodes/0/_state/segments_2c"))): This index was initially created with Lucene 8.x while the current version is 10.1.0 and Lucene only supports reading the current and previous major versions. This version of Lucene only supports indexes created with release 9.0 and later by default.
```

<br>

```JSON
security_exception: missing authentication credentials for REST request [/_nodes?filter_path=nodes.*.version%2Cnodes.*.http.publish_address%2Cnodes.*.ip]
```

<br>

# Kibana

```Bash
Kibana (v9.0.2) is incompatible with the following Elasticsearch nodes in your cluster: v7.17.28 @ 10.128.0.43:9200 (10.128.0.43)
```

<br>

# tmp

```Bash
builtins.ValueError: URL must include a 'scheme', 'host', and 'port' component (ie 'https://localhost:9200')
```

<br>

```Bash
configparser.NoOptionError: No option 'host' in section: 'output_elasticsearch'
```

<br>

```Bash
configparser.NoOptionError: No option 'pipeline' in section: 'output_elasticsearch'
```

<br>

```Bash
configparser.NoOptionError: No option 'type' in section: 'output_elasticsearch'
```

<br>

# tmp

```Text
Cannot connect to the Elasticsearch cluster currently configured for Kibana.

To use the full set of free features in this distribution of Kibana, please update Elasticsearch to the default distribution.
```