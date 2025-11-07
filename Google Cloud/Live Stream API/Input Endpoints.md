# Input Endpoint Overview

An input endpoint is an endpoint to which your encoder sends your input stream

* Can be used to specify configurations for a stream (*Input resolution*, *Input type*, *Video cropping*, *etc.*)

<br>

# Input Endpoint URI

An input endpoint consists of either an RTMP or SRT URI

<br>

RMTP URI
```Text
rmtp://ENDPOINT_IP/live/STREAM_ID
```

SRT URI
```Text
srt://ENDPOINT_IP:4201?streamid=STREAM_ID
```
