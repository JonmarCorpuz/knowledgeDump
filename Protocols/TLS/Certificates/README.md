# TLS Certificates Overview

TLS certificates are digital files used to verify the identity of a website while encrypting connections via HTTPS

* Contain various details of a website (*Domain name*, *Public key used for encryption*, *Issuing CA*, *Validity period*, *etc.*)

<br>

```YAML
--key-file=
--cert-file=
--peer-cert-file=
--peer-client-cert-auth=true
--peer-key-file=
--peer-trusted-ca-file=
--trusted-ca-file=
```