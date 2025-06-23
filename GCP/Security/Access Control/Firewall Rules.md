# Firewall Rule Overview


| Always Allowed Traffic |
| --- |
| Google Cloud metadata server traffic |
| Packets sent to an IP address assigned to one of a VM's own NICs where packets stay within the VM itself |

<br>

| Always Blocked Traffic |
| --- | 
| DHCP offers and acknowledgements (Applies to ingress packets to UDP on port 68 and 546) |
| All traffic other than external IPv4 and IPv6 using TCP, UDP, ICMP, ICMPv6, IPIP, AH, ESP, SCTP, and GRE (Applies to ingress packets to external IP addresses) |

<br>

# Firewall Rule Parameters

| Firewall Rule Parameter | Description |
| --- | --- |
| Direction | Either ingress or egress |
| Source | (Only applicable to ingress rules) |
| Destination | (Only applicable to egress rules) |
| Protocol | |
| Port | |
| Action | Either allow or deny |
| Priority | Between 0 and 65535 (Lower values have higher priority) |

<br>

| Firewall Rule Best Practice |
| --- |
| Use the model of least privilege |
| Minimize direct exposure to and from the Internet |
| Prevent ports and protocols from being exposed unnecessarily |
| Develop a standard naming convention for firewall rules |
| Consider service account firewall rules instead of tag-based rules |

<br>

# Implied Firewall Rules

Implied firewall rules are firewall rules that are present in all VPC networks

## Implied IPv4 Firewall Rules

| Implied IPv4 Firewall Rule | Description |
| --- | --- |
| Allow egress | Lets any instance send traffic to any destination |
| Deny ingress | Protects all instances by blocking incoming connections to them |

<br>

## Implied IPv6 Firewall Rules

| Implied IPv6 Firewall Rule | Description |
| --- | --- |
| Allow egress | Lets any instance send traffic to any destination | 
| Deny ingress | Protects all instances by blocking incoming connections to them |

<br>

# Default Firewall Rules

| Default Firewall Rule | Description |
| --- | --- |
| **default-allow-internal** | Allows ingress connections for all protocols and ports among instances within the VPC network |
| **default-allow-ssh** | Allows traffic on port 22 |
| **default-allow-rdp** | Allows traffic on port 3389 |
| **default-allow-icmp** | Allows ICMP traffic |