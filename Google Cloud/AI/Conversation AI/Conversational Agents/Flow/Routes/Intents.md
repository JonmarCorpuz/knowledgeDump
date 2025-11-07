# Route Intent Overview

An intent is the end-user's intention for one conversation turn

<br>

# Intent Components

## Labels

Labels help categorize intents 

<br>

| System Keyword | Description |
| --- | --- |
| head intent | The end-user's primary purpose for interacting with an agent |
| contextual | |
| agent assist head intent | |
| vague intent | |

<br>

| Driver | Description |
| --- | --- |
| driver:account | |
| driver:billing | |
| driver:payments | |
| driver:plans and features | |
| driver:scheduling | |
| driver:technical support | |
| driver:equipment | |

<br>

# Intent Parameters

An [intent parameter](https://cloud.google.com/dialogflow/cx/docs/concept/parameter#intent) refers to a specific piece of information or data that the agent extracts from the end-user's input as part of understanding the user's intent

* Defined at design-time when creating intent data or when creating annotating training phrases
* Can be used in static fulfillment response messages of intent routes
* Reference an intent parameter to the current matched intent using either `$intent.params.PARAMETER_ID.original` or `$intent.params.PARAMETER_ID.resolved`

<br>

| Intent Parameter Component | Description |
| --- | --- |
| Entity Type | The entity type associated with the parameter |
| Is List | |
| Redact in log | |

<br>
