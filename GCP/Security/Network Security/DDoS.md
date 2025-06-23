# Distributed Denial of Service Overview

<br>

# DDoS Mitigations

## Cloud Load Balancing

* Provides built-in defense against infrastructure DDoS attacks
* No additional configuration is required to activate this DDoS defense
* Leverages Google's central DDoS mitigation service (It can configure load balancers to drop or throttle traffic if the system detects an attack)

<br>

## Cloud CDN

* Caches content between users and servers
* Requests for cached content are routed to POPs
* Google's massive infrastructure can absorb attacks

<br>

## API Gateway

* Throttle requests to limit requests from clients
* Control access to APIs from a single location
* Allows API monitoring

<br>

## Cloud Armor

* Mitigates infrastructure DDoS attacks using load balancers (**Global external application load balancers**, **Regional external application load balancers**, **Classic application load balancers**, **External proxy network load balancers**)
* Allows and blocks traffic while ensuring rate limits based on IP, geolocation, and custom match parameters
* Defends against application layer attacks with OWASP Top 10
* Decisions are logged to Cloud Logging and Monitoring dashboard, and Cloud Security Command Center