# Route Fulfillment Overview

A fulfillment refers to the process where an agent carries out an action in response to a user input or intent

* Enables the conversational agent to respond to an end-user's input
* Used everywhere that a response message is needed (*Page entry fulfillment*, *Routes*, *Event handlers*, *Initial prompts for forms*, *etc.*)

<br>

# Agent Response

## Static Responses

A [static response](https://cloud.google.com/dialogflow/cx/docs/concept/fulfillment#text) message sends text dialogue to the end-user (If the user's detect intent API calls or integratioon use speech synthesis then this text will be used to generate audio content)

* Can contain parameter references and inline system functions

<br>

## Parameter References

A [parameter](https://cloud.google.com/dialogflow/cx/docs/concept/parameter) is structured data that can easily be used to perform some logic or generate responses

* Used to capture and reference values that have been supplied by the end-user during a session

<br>

| Parameter Value Type | Description |
| --- | --- |
| Scalar | A single numeric or string value |
| Composite | A JSON object populated by matching a [composite entity](https://cloud.google.com/dialogflow/cx/docs/concept/entity-options#comp) or by fillin an [intent parameter](https://cloud.google.com/dialogflow/cx/docs/concept/parameter#:~:text=filling%20of%20an-,intent%20parameter,-%2C%20which%20contains%20original) that contains `original` and `resolved` fields |
| List | A list of scalar or composite values populated for a parameter configured as a list |
| Null | The parameter has not been set (`null`) | 
| Empty String | The value is set to an empty string (`""`) |

<br>

| Parameter Definition | Description |
| --- | --- |
| **Define at design-time** | Using either the console or the API to define parameters during design-time |
| **Reference at design-time** | Parameters references are variables that hold parameter values to be extracted at runtime (The user uses either the console or the API to reference parameters in various data types) |
| **Set at runtime** | The agent service, the customer's service that calls the API, and their webhook service can all set parameter values at runtime |
| **Get at runtime** | The parameter references contain the parameter values that have been set and the user can either use the API or a webhook to get the parameter values at runtime |

## Inline System Functions

<br>

## Webhook Calls

<br>

## Parameter Presets