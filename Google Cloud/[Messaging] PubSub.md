# Pub/Sub Overview

[Pub/Sub](https://cloud.google.com/pubsub/docs/overview) is an asynchronous and scalable messaging service where the senders of messages are decoupled from the receivers of messages

* Allows services to communicate asynchronously (With latencies of 100 milliseconds)
* Used for streaming analytics and data integration pipelines to load and distribute data (Equally effective as a messaging-oriented middleware for service integration or as a queue to parallelize tasks)

<br>

# Pub/Sub Components

```Text
Publisher --> Message --> Topic --> Subscription --> Subscriber
Schema ----------------->
```

## Topic

A topic is a named entity that represents a feed of messages

<br>

## Publishers

A publisher (producer) creates messages and sends (publishes) them to the messaging service on a specific topic

<br>

## Subscription

A subscription is a named entity that represents an interest in receiving messages on a particular topic

<br>

## Subscribers

A subscriber (consumer) is what receives messages on a specified subscription

<br>

## Message

A message is the data that moves through the service

<br>

## Schema

A schema is a named entity that governs the data format of a Pub/Sub message