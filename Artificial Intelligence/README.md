# Artificial Intelligence Overview

* Data driven ("*Without data, you're just another person with an opinion*" - William Edwards Deming)
* Data always comes in raw and cleaning that data allows you to learn more about the data itself

<br>

Generic recipe
```Text
1. Specification of the data you want to utilize
2. Choosing the appropriate AI model/architecture to use
3. Choice of an objective/cost/loss function
4. Choice of an initial parameter set for the model
5. Choice of an optimization routine
6. Training and validating your AI model/infrastructure
7. Testing your AI model/infrastructure
8. Hardening your AI model/infrastructure against adversarial attacks
```

<br>

Questions to ask to know more about your data
```Text
1. Stationary or non-stationary
2. Parametric or non-parametric
3. Markovia vs non-Markovian (Is the conditional probability of a future state only dependent on the present state or not)
```

<br>

Additional questions
```Text
Q: Are markets Markovian?
Q: What is relevant during a knee-jerk reaction
Q: What is still relevant when going through a regime change? (Learning with rejection to help not making decisions anymore based on what is not relevant anymore)
```

<br>

Types of datasets
* Tick data/Time series (Ex: *Signal extraction*, *Data mining*, *etc.*)
* Market data and holding data (Ex: *Asset management*, *etc.*)
* Alternative data (Ex: *Data collected by IoT*)
* Categorical data
* Text (Ex: *Classification*, *etc.*)
* Images (Ex: *Computer vision*, *etc.*)
* Sound (Ex: *Voice recognition*, *etc.*)
* Video (Ex: *Motion detection*, *etc.*)
* etc.

<br>

Collecting, generating, cleaning, pre- and post-processing, and picking datasets
```Text
1. Collecting and cleaning raw data for training (Removing unrelevant data, etc.)
2. Generating more data for training (In many cases, you might not have enough data for training)
3. Generating labels (Supervised learning)
4. Proper data classification
5. Imputation for missing data
```

<br>

Cleaning raw data (*If you give me enough parameters, I can always fit the data*)
* Create a training set, then convert that into a validation set (To avoid over-fitting in order to avoid forcing your AI model to that data), and then convert that into a test set
