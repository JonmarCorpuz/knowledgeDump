# Application Deployment Overview

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Blue/Green Deployment

The blue/green deployment is a deployment strategy used to reduce downtime and risk by running two environments

* Provides reduced downtime, easy rollback, safer releases, and seamless user experience

| Environment | Description |
| --- | --- |
| Blue | The deployment running the current live version of the application that's serving users |
| Green | The deployment running the new version of the application that's being deployed and tested without affecting the users in the Blue environment (Once everything has been verified, traffic is switched from the Blue environment to the Green environment) |

* The traffic switch is typically done using load balancers or routing mechanisms
* The traffic switch can happen instantly or gradually
* After the traffic switch, the Green environment becomes the new Blue environment, while the old Blue environment becomes idle and can be used as a backup in case you need to rollback 

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Canary Deployment

A canary deployment is a deployment strategy where a new version of an application is rolled out to a small, specific subset of users or servers before it's fully rolled out to the entire user base or infrastructure

* Provides small initial rollouts (1% to 5% of traffic or users is directed to the new version of the application
* Allows you to increase the rollout increments if the canary deployment is successful until all users are transitioned to the new version
* If problems are detected during the canary phase, the canary version can be rolled back to the previous stable version for the affected subset of users, without affecting the rest of the user base (This minimizes the risk of a bad deployment affecting the entire system)
* Reduces the risk of widespread issues 
