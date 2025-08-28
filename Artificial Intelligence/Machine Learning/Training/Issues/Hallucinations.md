# AI Hallucinations Overview

[AI hallucinations](https://cloud.google.com/discover/what-are-ai-hallucinations?hl=en) are incorrect or misleading results that AI models generate (*Incorrect predictions*, *False positives*, *False negatives*, *etc.*)

* Can be caused by a variety of factors (*Insufficient training data*, *Incorrect assuptions made by the model*, *Biases in the training dataset*, *Lack of proper grounding*, *etc.*)

<br>

# How AI Hallucinations Work

* The accuracy on AI predictions often depends on the quality and completeness of the training data (If the training data is incomplete, biased, or flawed then the AI model may learn incorrect patterns leading to inaccurate predictions or hallucinations)
* The lack of grounding can cause a model to generate outputs that are actually factually incorrect, irrelevant, or nonsensical

<br>

# Preventing AI Hallucinations

* Limit the number of possible outcomes that the model can predict using **regularization** (Regularization penalizes the model for making predictions that are too extreme in order to prevent the model from overfitting the training data and making incorrect predictions)
* Only use data that's relevant to the task that the model will be performing (Using data that's not relevant to the task can lead to the AI model making incorrect predictions)
* Create a template (*Title*, *Introduction*, *Body*, *Conclusion*, *etc.*) for the model to follow
* Tell the model what you want and don't want (*By providing feedback to the model*, *etc.*)