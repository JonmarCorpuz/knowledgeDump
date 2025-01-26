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
* The primary downside is the need for double resources since both environments run concurrently

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

