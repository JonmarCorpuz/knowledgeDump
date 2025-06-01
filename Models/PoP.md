# Pyramid Of Pain Overview

It’s a pyramid-shaped diagram that categorizes Indicators of Compromise based on how much they impact an attacker if you detect or block them (The higher you go on the pyramid, the more it hurts the attacker, but also the harder it is to detect) <br>

# PoP Categories

![](https://github.com/JonmarCorpuz/knowledgeVault/blob/main/Models/Images/pyramid-of-pain.jpg)

## TTPs
<br>

* Description: Behavioral patterns (How attackers operate)
* Pain to attacker: Very High
* Reasoning: TTPs reflect habits and workflows so changing these means reengineering the entire attack strategy, training operators, and testing new methods

## Tools
<br>

* Description: Actual malware, hacking frameworks, or scripts used by attackers
* Pain to attacker: High
* Reasoning: The attacker may need to rewrite or switch to new tools

## Artifacts

* Description: Technical clues left on systems or networks
* Pain to attacker: Medium
* Reasoning: Changing artifacts often requires modifying scripts, tools, or procedures

| Artifact Type | Description |
| --- | --- |
| Host Artifact | Traces or observables that attackers leave on the system (*Registry values*, *Files*, *etc.*) |
| Network Artifact |  |

## Domain Names
<br>

* Description: Malicious domains used to host malware or phishing sites
* Pain to attacker: Low to medium
* Reasoning: Registering a new domain takes more effort and time than changing an IP address

## IP Addresses
<br>

* Description: Specific IP addresses used for malicious activity
* Pain to attacker: Low
* Reasoning: Attackers can easily switch IPs

## Hash Values

* Description: Unique digital fingerprints of files
* Pain to attacker: Very low
* Reasoning: Attackers can easily recompile or slightly modify a file to change its hash
