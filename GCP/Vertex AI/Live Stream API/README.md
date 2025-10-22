# Live Stream API Overview

GCP's Live Stream API is a service that transcodes mezzanine live video signals into consumer-friendly streaming formats (*HLS*, *DASH*)

```Text
Input Stream --> [GCP Project (Live Stream API) --> (Cloud Storage) --> (Content Delivery Network)] --> Output Stream
```

<br>

# Supported Features

* Automatic infrastructure provisioning
* Integration with Cloud Storage, Cloud Audit logs, and Google Cloud infrastructure
* Configuration of a backup input stream for redundancy
* Live to video on demand (VOD)
* Content encryption

<br>

# Supported Inputs

* Protocols (*SRT*, *RTMP*)
* Video codecs (*H.2648*)
* Audio codecs (*AAC*)
* Captions (*Embedded CEA-608/708*)

<br>

# Supported Outputs

* Protocols (*Apple HLS with fMP4 and MPEG2-TS segments*, *MPEG-DASH with fMP4 segments*)
* Video codecs (*H.2648*)
* Audio codecs (*AAC*)
* Captions (*Embedded CEA-608/708*)
* Encryption (*AES-123*, *SAMPLE-AES*, *MPEG-CENC*)
* Spritesheet images (*JPG tiles*, *Single images*)