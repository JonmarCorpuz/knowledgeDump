# Service Level Objective Overview

An SLO represents a specific target level of service performance that's measurable and is agreed upon between a provider and the service consumers

* Above the specified threshold, almost all users should be happy with your service (Below the threshold, users are likely to start complaining or to stop using the service)
* Customers won't ever be able to experience 100% reliability because the chain of systems between you and your customers is often long and complex, and any of those components can fail (This means that you can't always have 100% reliability but rather you can have 99%, 99.9%, 99.99%, etc. reliability, where each extra nine comes at an increased cost while the marginal utility to your customers steadily approaches zero)
* Reliability of 100% isn't an engineering culture SLO, it's an operations team SLO (Once you have an SLO target below 100%, it needs to be owned by someone in the organization who is empowered to make tradeoffs between feature velocity and reliability)
* Usually, the number one source of outages is change (*Pushing new features*, *Applying security patches*, *Deploying new hardware*, *Scaling up to meet customer demand*, *etc.*)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Service Level Objective Metrics

## Service Level Indicator

An SLI is a metric used to quantitatively measure the performance of a service

* Generally recommended to threat the SLI as the ratio of two numbers: `The number of good events / The total number of events` (*Number of successful HTTP requests/Total HTTP requests*, *Number of search results that used the entire corpus/Total number of search results*, *etc.*)
* Ranges from 0% to 100% (0% means nothing works and 100% means nothing is broken)
* Serves as a key element in managing and understanding the quality of services provided
* Focuses on specific aspects of the service that are important to the users and the business (*Response time*, *Availability*, *Error rate*, *Throughput*, *etc.*)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Error Budget

* The error budget is 100% minus the SLO (Ex: *If your SLO is 99.9% for a service that receives 3 million requests over a four-week period and has a budget of 0.1%, this would mean that a single outage that's responsible for 1500 erros would cost 50% of the error budget)
