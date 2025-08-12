# MLOps With Verex AI Overview

<br>

MLOps workflow
```Text
ML development --> Continuous model training --> Model deployment to make predictions --> Continuously monitor the model to ensure that its performance is improviing --> Model management
```

<br>

MLOps workflow automated by Vertex AI in a serverless manner using containers which supports both FKP and TFX (Vertex AI pipeline)
```Text
ML Development (Create a dataset in Vertex AI)
|
|-->  Continuous Training (Use this tabular dataset and use AutoML to apply a classification model on it)
  |
  |--> Model Deply (Get evaluation metrics on that model and we then decide whether or not we'd want to deploy this model or not based on those metrics)
    |
    |--> Deploy this model to an endpoing using Vertex Predictions
```