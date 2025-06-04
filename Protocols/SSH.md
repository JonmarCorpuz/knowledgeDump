# SSH Overview

Secure SHell is a network protocol that's used to remotely access and control computers over a network

* Encrypted by default

<br> 

# SSH Server

<br>

# SSH Client

<br>

# SSH Key Pairs

## Public Key

* Can be shared freely without any negative consequences
* Used to encrypt messages that only the private key can decrypt
* This key is uploaded to the SSH server that the SSH client wants to SSH to (Their public key is stored in `~/.ssh/authorized_keys`)

## Private Key

* Retained by the SSH client and should be kept secret (Any compromise of the private key will allow the attacker to log into servers that are configured with the associated public key without additional authentication)

<br>

# Fingerprint

Fingerprinting is a security step that helps make sure you're connecting to the right machine

* Protects users from MiTM attacks
* The first time you connect to a server, your computer shows its fingerprint and asks if you want to connect to the server (If yes, your machine will save that fingerprint in the `known_hosts` file)

## Fingerprint

A fingerprint is a short hashed version of the SSH server's public key

<br>

# References

[1] https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server#how-do-ssh-keys-work <br>