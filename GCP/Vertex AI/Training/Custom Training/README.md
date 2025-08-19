# Custom Training Job Overview

Custom training is the process of training machine learning models using your own algorithms and data

* Running a custom training job is done with containers on Vertex AI
* Allows users to create a training application that's optimized for their trageted outcome (Users have complete control over training application functionality)
* Users have full control and flexibility over the model architecture, framework, and training code

<br>

```Text
1. Export notebook to a Python file (You can use the nbconvert tool)
2. Update the code to read data from Cloud Storage and write the model to Cloud Storage so that we can access it later on
3. Containerize the code that the Vertex AI training will execute
4. Launch the training job
```