# Grounding Overview

[Grounding](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/overview#:~:text=In%20generative%20AI%2C%20grounding%20is,of%20the%20model%20inventing%20content.) refers to the process of ensuring that a large language model's output are explicitly connected to trusted data sources rather than relying only on the model's pre-trained internal information

* Important for situations where accuracy and reliability are significant
* The system first determines if the input query can be answered solely with the model's built-in knowledge or if it requires grounding with up-to-date information (If grounding is needed then relevant information from trusted external sources will be retrieved) 

<br>

Grounding benefits
* Improves factual accuracy and relevance by supplementing the model's knowledge with real verifiable data
* Reduces hallucinations since the response is anchored to explicit external sources rather than just learned information
* Increases trust since citations and references can be provided allowing users to verify the responses

<br>

# Grounding Methods

## Retrieval-Augmented Generation Overview

[RAG](https://cloud.google.com/use-cases/retrieval-augmented-generation?hl=en) is an AI framework where the model retrieves relevant documents and includes their content for context before generating its answer 

* Combines the strenghs of traditional information retrieval systems with the capabilities of generative LLMs to provide mode accurate and up-to-date information