# Custom Training Job Overview

* Running a custom training job on Vertex AI is done with containers

<br>

```Text
1. Export notebook to a Python file (You can use the nbconvert tool)
2. Update the code to read data from Cloud Storage and write the model to Cloud Storage so that we can access it later on
3. Containerize the code that the Vertex AI training will execute
4. Launch the training job
```