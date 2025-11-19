# Retrieval-Augmented Generation Overview

[RAG](https://cloud.google.com/use-cases/retrieval-augmented-generation?hl=en) is an AI framework where the model retrieves relevant documents and includes their content for context before generating its answer 

* Combines the strenghs of traditional information retrieval systems with the capabilities of generative LLMs to provide mode accurate and up-to-date information
* Prevents LLMs from sharing outdated and potentially inaccurate responses that are limited to their pre-trained data 
* Provides several advantages augmenting traditional methods of text generation when dealing 

<br>

# How RAG Works

* Leverages powerful search algorithms to query external data and once the data is retrieved then the relevant information undergoes pre-rpocessing (*Tokenization*, *Stemming*, *Removal of stop words*, *etc.*)
* The pre-processed retrieved information is then seamlessly incorporated into the pre-trained LLM in order to enhance the LLM's context and provide it with a more comprehensive understanding of the topic