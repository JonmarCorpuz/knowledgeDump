# OS Login Overview

[OS Login](https://cloud.google.com/compute/docs/oslogin) simplifies SSH access management by linking your Linux user account to your Google identity

* Automatically ties a Linux user account to a user's Google identity (The same Linux account information is used across all instances in the same project or organization)
* User permissions are updated automatically when an administrator changes IAM permissions for a Google identity (Google checks permissions for every login attempt to prevent unwanted access)
* Linux account information can be synchronized from AD and LDAP (2FA can be enabled as well)
* Provides audit logging to help monitor connections to VMs for OS Login users

<br>

# How OS Login Works

* Compute Engine performs configurations on VMs and the Google accounts of OS Login users
* Compute Engine deletes the VM's `authorized_keys` files and automatically configures an OpenSSH server (The SSH server will retrieve the SSH keys associated with the Linux user account to authenticate the login attempt)
* Users can still configure an `authorized_keys` file for local user accounts even when OS Login is enabled (Local user accounts must have a different username and UID than OS Login users)
* Automatically configures POSIX accounts (*Username using the USERNAME_DOMAIN_SUFFIX format*, *A randomly generated and unique POSIX-compliant UID*, *A POSIX-compliant GID that's the same as the UID*, *The path to the user's home directory*)

<br>

# Setting Up OS Login

* Enabling OS Login requires the `enable-oslogin: TRUE` key value pair in either the project's and VM's metadata
* 2FA can be enabled for OS Login using the `enable-oslogin-2fa` key value pair