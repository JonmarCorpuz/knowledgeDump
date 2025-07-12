# Certificate Signing Overview

<br>

# Certificate Signing Workflow

## 1. Generate Keys

The website owner or admin generates a private and public key pair

| Key | Description |
| Private Key | A secret key used to decrypt or sign certificates (Helps prove a server's identity) |
| Public Key | A publicly shared key used to encrypt and verify certificates (Helps clien machines encrypt data to the server) |

<br>

## 2. Certificate Signing Request 

The owner or admin creates a CSR which contains the public key, domain name, organization information, and digital signature that was created using the private key

<br>

## 3. Send the Certificate Signing Request to a Certificat Authority

* The CSR is sent to a trusted CA for validation

<br>

## 4. The Certificate Authority Verifies the Identity

<br>

## 5. Certificate Authority Issues a Digital Certificate



<br>

## 6. Install the Certificate

The owner or admin installs the certificate onto their web server