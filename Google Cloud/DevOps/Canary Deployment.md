# Canary Deployment

A canary deployment is a deployment strategy where a new version of an application is rolled out to a small, specific subset of users or servers before it's fully rolled out to the entire user base or infrastructure

* Provides small initial rollouts (1% to 5% of traffic or users is directed to the new version of the application
* Allows you to increase the rollout increments if the canary deployment is successful until all users are transitioned to the new version
* If problems are detected during the canary phase, the canary version can be rolled back to the previous stable version for the affected subset of users, without affecting the rest of the user base (This minimizes the risk of a bad deployment affecting the entire system)
* Reduces the risk of widespread issues

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)
