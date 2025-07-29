# Service Account Token Overview

<br>

Create a token for a service account
```Bash
kubectl create token SERVICE_ACCOUNT_NAME
```

Decode a token
```Bash
jq -R 'split(".") | select(length > 0) | .[0],.[1] | @base64d | fromjson' <<< TOKEN
```

<br>

# TokenRequest API
