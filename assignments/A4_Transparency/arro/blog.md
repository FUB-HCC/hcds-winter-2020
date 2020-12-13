# Assignment 4
> **Name:** `arro` Arne Rolf
> **Session:** [05 Exercise - Transparency](https://github.com/FUB-HCC/hcds-winter-2020/wiki/05_exercise)   
----

## R5 - Reflection
> **Date:** 06.12.2020 - 21:39 PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> **Book:** "Interpretable machine learning. A Guide for Making Black Box Models Explainable" by Molnar

### 🗨️&nbsp; "How does the reading inform your understanding of human-centered data science?"  
This book chapter about interpretability was a good recap and addition to the content of the lecture.
They mentioned that intrinsic interpretability can be applied to models with short decision trees, so I guess this means the amount of layers of a model. Sadly ,they didn't provide a ballpark figure on how many layers this would be feasible to do.

### ❓&nbsp; Questions
1. Is the method "Intrinsically interpretable model" meant to dissect the model layers to be able to look at each individual outcome? If so, is the model to be analyzed recreated as a new second model with the same layer parameters but with the learned weights from the first model?

**Why:** ...

***

## A4 - Transparency
> **Date:** 06.12.2020 - 21:39 PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> Group: Arne Rolf (`arro`) and Malina S. (`masc`) and Marc O. (`maop`)<br>
> Model: `goodfaith`<br>

### Summary 

_Please summarize your findings and analyses regarding (1) general understanding, (2) API, (3) ML algorithm and training/test data, and (4) features._

### (1) general understanding

The ORES review tool is the key user-facing feature of the ORES extension, which provides objective revision evaluation services to automatically rate a revision's characteristics. In this section we will discuss the model `goodfaith` which predicts the likelihood of an article's revertions of being good faith.

### (2) API

### (3) ML algorithm and training/test data

We were able to find out what Machine Learning Algorithm is being used through the provided API request. We found out, that the underlaying algorithm is called `GradientBoosting`. This is a machine learning technique for regression and classification problems, which produces a prediction model in the form of an ensemble of weak prediction models, typically decision trees. It builds the model in a stage-wise fashion like other boosting methods do, and it generalizes them by allowing optimization of an arbitrary differentiable loss function. This algortithm Gradient boosting can be used in the field of learning to rank. It uses the ` friedman_mse` (Friedman Mean Squared Error) criterion. The used loss function is called `deviance`. In fact, we had difficulties distinguishing between the `friedman_mse` and `deviance` terms. `friedman_mse` We figured out that the default value of ‘friedman_mse’ is generally the best as it can provide a better approximation in some cases. When it comes to loss functions, the goal of those is to be optimized. The term `deviance` is refering to deviance (= logistic regression) for classification with probabilistic outputs.

Analyzing the model performance we dived deeper into the metrics provided by the `model_info` API call. It contains information about basic performance measurements (i.e. Precision, Rates, Recall, Damaging and true/false positive/negative values (Confusion Matrix). The Algorithm makes use of these common performance measurement metrics. Although it is not clear if an exclamation mark in front of a parameter refers to its negation, the model_info query provides a detailed overview of used classification methods. Also we are still unsure about how the algorithm applies so called micro and macro values to its test set. It is unclear to us what metric is the most powerful. Therefore an interpretation of performance in consideration of the resulting data which has been applied to the algorithm previously cannot be made with certainty.

Having a closer look to the training and test data it is necessary to look closer into the ORES documentation and other ressources: Halfaker et. al. states, that “ORES is a collection of machine classifier models and an API […] [the models are] using varied sources of training data” [ref](https://www-users.cs.umn.edu/~halfaker/files/halfaker18ores.pdf). Although test and training data is supposed to be found on [GitHub](https://github.com/wikimedia/ores), we were not able to gain insights of the data.

![IMG](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A4_Transparency/arro/Bildschirmfoto%20.png)

### (4) features

The model is using roughly 80 different features. Such as `feature.english.badwords`, `feature.english.informals`, `feature.revision.user.is_anon`, `feature.revision.diff.longest_new_repeated_char`, `feature.temporal.revision.user.seconds_since_registration` etc.
It is assumed that the following features are playing an important role in ORES classifications: `feature.english.badwords` (checks if the reversion of an article is containing bad words (e.g. informal words)) and `feature.revision.user.is_anon` (checks if the revision of an article has been made by an anonymous user). We believe that this plays an important role because the classification strongly depends on whether the change was made by a "trusted" user (the longer an user has been contributing to Wikipedia the less likely it is that the user acted out of malice) and whether the article was written in a high linguistic standard which is virulent for maintaining Wikipedia article's quality.



### Openness
...

### Intrinsic interpretability
...

### Algorithmic transparency
...

### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_
