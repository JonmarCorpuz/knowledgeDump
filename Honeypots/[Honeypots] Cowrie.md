# Cowrie Overview

Cowrie is an interaction honeypot designed to emulate an SSH and Telnet server

* Helps log brute-force attacks and capture the actions of attackers once they gain shell access (Every command by the attacker is recorded)
* Acts as a real SSH or Telnet server with a fake file system
* Downloads and stores any unique files the intruder tries to fetch but won't execute them
* Uploaded content isn't persistent
* You can configure the contents of certain files so the honeypot can pretend to be a specific target
* Records all of the SSH tunneling requests received by the honeypot but won't forward them to their destination

<br>

# Cowrie Logs

* The Cowrie logs can be found at `/home/cowrie/honeypot/var/log/cowrie`

<br>

# Bot Identification

* The data recorded by Cowrie can be used to identify individual bots (Some artifacts tend to be consistent across bots)