# Title of your post
> **Name:** `albe` Ali Bektas
> **Session:** [05 Exercise - Transparency](https://github.com/FUB-HCC/hcds-winter-2020/wiki/05_exercise)   
----

## R5 - Reflection
> **Date:** DD.MM.YYYY - HH:MM PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> **Book:** "Interpretable machine learning. A Guide for Making Black Box Models Explainable" by Molnar

### 🗨️&nbsp; "How does the reading inform your understanding of human-centered data science?"  
_Answer in at least 2-3 complete sentences_<br>

The book chapter informs about different characteristics of methods for interpreting ml models.   
It is differentiated between *Intrinstic* and *Post hoc* methods where it is differenciated wheather a method looks inside the models 
internal (e.g. stored parameters) or if the interpretation is done after the model is trained. As a further characteristic of interpretation methods it is differentiates wheather if the method can only be used for specific types of models: *model-specific* or if can be applied to any kind of model: *model-agnostic*. As a further characteristic the scope of a method is differentiated. If the interpretation is for individual predictions, the entiere model behavior or in between. 

### ❓&nbsp; Questions

1. I am not sure if I understood the categorization of an *Intrinstic* method correct. 

It is meantioned that the intrinstic method is archived by restricting the complexity of a model. By reading this I understand that intrinstic interpreatability is possible when choosing a simple model (e.g. linear regression). 

It is also mentioned that for intrinsically interpretable models the models internals (e.g. the learned weights) are inspected and tried to be explained . So do I got it right? Is the a criteria for an interpretation method to be characterized as *Intrinsic* that it is used for models with simple complexity and where the models internals are viewed?

**Why:** ...
I am asking this because I understand that per this definition Convolutional Neural Networks falls also to the *Intrinstic* interpretable models because of its learned weights and biases. But when I am thinking of some deep CNN's I cannot imagine these to be less complex.y.  

***

## A4 - Transparency
> **Date:** DD.MM.YYYY - HH:MM PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> Group: PERSON1 and PERSON2<br>
> Model: NAME OF MODEL<br>

### Summary 

_Please summarize your findings and analyses regarding (1) general understanding, (2) API, (3) ML algorithm and training/test data, and (4) features._

`https://ores.wikimedia.org/v3/scores/`

The reverted model is available in  20  projects. Mainly in version 0.5.0

|     | model    | project      | version   |
|----:|:---------|:-------------|:----------|
|   3 | reverted | bnwiki       | 0.5.0     |
|  13 | reverted | elwiki       | 0.5.0     |
|  21 | reverted | enwiktionary | 0.5.0     |
|  46 | reverted | glwiki       | 0.5.0     |
|  49 | reverted | hrwiki       | 0.5.0     |
|  52 | reverted | idwiki       | 0.5.0     |
|  53 | reverted | iswiki       | 0.5.0     |
|  91 | reverted | tawiki       | 0.5.0     |
|  98 | reverted | testwiki     | 0.0.3     |
| 108 | reverted | viwiki       | 0.5.0     |
| 117 | reverted | bnwiki       | 0.5.0     |
| 127 | reverted | elwiki       | 0.5.0     |
| 135 | reverted | enwiktionary | 0.5.0     |
| 160 | reverted | glwiki       | 0.5.0     |
| 163 | reverted | hrwiki       | 0.5.0     |
| 166 | reverted | idwiki       | 0.5.0     |
| 167 | reverted | iswiki       | 0.5.0     |
| 205 | reverted | tawiki       | 0.5.0     |
| 212 | reverted | testwiki     | 0.0.3     |
| 222 | reverted | viwiki       | 0.5.0     |

`https://ores.wikimedia.org/v3/scores/enwiki?models=YOURMODELNAME&model_info`
`https://ores.wikimedia.org/v3/scores/enwiki/REVID/YOURMODELNAME?model_info`

Following is an overview of the information each properties provides on an model: 

|    | params                   | environment           | statistics   | score_schema   |
|---:|:-------------------------|:----------------------|:-------------|:---------------|
|  0 | ccp_alpha                | machine               | !f1          | properties     |
|  1 | center                   | platform              | !precision   | title          |
|  2 | criterion                | processor             | !recall      | type           |
|  3 | init                     | python_branch         | accuracy     |                |
|  4 | label_weights            | python_build          | counts       |                |
|  5 | labels                   | python_compiler       | f1           |                |
|  6 | learning_rate            | python_implementation | filter_rate  |                |
|  7 | loss                     | python_revision       | fpr          |                |
|  8 | max_depth                | python_version        | match_rate   |                |
|  9 | max_features             | release               | pr_auc       |                |
| 10 | max_leaf_nodes           | revscoring_version    | precision    |                |
| 11 | min_impurity_decrease    | system                | rates        |                |
| 12 | min_impurity_split       | version               | recall       |                |
| 13 | min_samples_leaf         |                       | roc_auc      |                |
| 14 | min_samples_split        |                       |              |                |
| 15 | min_weight_fraction_leaf |                       |              |                |
| 16 | multilabel               |                       |              |                |
| 17 | n_estimators             |                       |              |                |
| 18 | n_iter_no_change         |                       |              |                |
| 19 | population_rates         |                       |              |                |
| 20 | presort                  |                       |              |                |
| 21 | random_state             |                       |              |                |
| 22 | scale                    |                       |              |                |
| 23 | subsample                |                       |              |                |
| 24 | tol                      |                       |              |                |
| 25 | validation_fraction      |                       |              |                |
| 26 | verbose                  |                       |              |                |
| 27 | warm_start               |                       |              |                |


Here is an overview about the parameters of the model "reverted" for the wikipedia project "hrwiki":

|    | param                    | value         |
|---:|:-------------------------|:--------------|
|  0 | ccp_alpha                | 0.0           |
|  1 | center                   | 1.0           |
|  2 | criterion                | friedman_mse  |
|  3 | init                     |               |
|  4 | label_weights            | {'false': 10} |
|  5 | labels                   | [True, False] |
|  6 | learning_rate            | 0.01          |
|  7 | loss                     | deviance      |
|  8 | max_depth                | 3             |
|  9 | max_features             | log2          |
| 10 | max_leaf_nodes           |               |
| 11 | min_impurity_decrease    | 0.0           |
| 12 | min_impurity_split       |               |
| 13 | min_samples_leaf         | 5             |
| 14 | min_samples_split        | 2             |
| 15 | min_weight_fraction_leaf | 0.0           |
| 16 | multilabel               | False         |
| 17 | n_estimators             | 500           |
| 18 | n_iter_no_change         |               |
| 19 | population_rates         |               |
| 20 | presort                  | deprecated    |
| 21 | random_state             |               |
| 22 | scale                    | True          |
| 23 | subsample                | 1.0           |
| 24 | tol                      | 0.0001        |
| 25 | validation_fraction      | 0.1           |
| 26 | verbose                  | 0             |
| 27 | warm_start               | False         |


Here is an overview about the environment properties of the model "reverted" for the wikipedia project "hrwiki":

|    | environment property   | value                                        |
|---:|:-----------------------|:---------------------------------------------|
|  0 | machine                | x86_64                                       |
|  1 | platform               | Linux-4.9.0-11-amd64-x86_64-with-debian-9.12 |
|  2 | processor              |                                              |
|  3 | python_branch          |                                              |
|  4 | python_build           | ['default', 'Sep 27 2018 17:25:39']          |
|  5 | python_compiler        | GCC 6.3.0 20170516                           |
|  6 | python_implementation  | CPython                                      |
|  7 | python_revision        |                                              |
|  8 | python_version         | 3.5.3                                        |
|  9 | release                | 4.9.0-11-amd64                               |
| 10 | revscoring_version     | 2.8.0                                        |
| 11 | system                 | Linux                                        |
| 12 | version                | #1 SMP Debian 4.9.189-3+deb9u1 (2019-09-20)  |


We checked if the stats are realy the same as the general modelinfo API call provides for the reverted model. We can confirm that it does provide consistent information.

|    | metrics              | value                                                                           |
|---:|:---------------------|:--------------------------------------------------------------------------------|
|  0 | !f1 (labels)         | {'false': 0.494, 'true': 0.919}                                                 |
|  1 | !f1 (macro)          | 0.707                                                                           |
|  2 | !f1 (micro)          | 0.527                                                                           |
|  3 | !precision (labels)  | {'false': 0.347, 'true': 0.986}                                                 |
|  4 | !precision (macro)   | 0.666                                                                           |
|  5 | !precision (micro)   | 0.398                                                                           |
|  6 | !recall (labels)     | {'false': 0.855, 'true': 0.862}                                                 |
|  7 | !recall (macro)      | 0.858                                                                           |
|  8 | !recall (micro)      | 0.855                                                                           |
|  9 | accuracy (labels)    | {'false': 0.861, 'true': 0.861}                                                 |
| 10 | accuracy (macro)     | 0.861                                                                           |
| 11 | accuracy (micro)     | 0.861                                                                           |
| 12 | counts (labels)      | {'false': 18232, 'true': 1452}                                                  |
| 13 | counts (n)           | 19684                                                                           |
| 14 | counts (predictions) | {'false': {'false': 15708, 'true': 2524}, 'true': {'false': 211, 'true': 1241}} |
| 15 | f1 (labels)          | {'false': 0.919, 'true': 0.494}                                                 |
| 16 | f1 (macro)           | 0.707                                                                           |
| 17 | f1 (micro)           | 0.886                                                                           |
| 18 | filter_rate (labels) | {'false': 0.195, 'true': 0.805}                                                 |
| 19 | filter_rate (macro)  | 0.5                                                                             |
| 20 | filter_rate (micro)  | 0.244                                                                           |
| 21 | fpr (labels)         | {'false': 0.145, 'true': 0.138}                                                 |
| 22 | fpr (macro)          | 0.142                                                                           |
| 23 | fpr (micro)          | 0.145                                                                           |
| 24 | match_rate (labels)  | {'false': 0.805, 'true': 0.195}                                                 |
| 25 | match_rate (macro)   | 0.5                                                                             |
| 26 | match_rate (micro)   | 0.756                                                                           |
| 27 | pr_auc (labels)      | {'false': 0.992, 'true': 0.527}                                                 |
| 28 | pr_auc (macro)       | 0.76                                                                            |
| 29 | pr_auc (micro)       | 0.956                                                                           |
| 30 | precision (labels)   | {'false': 0.986, 'true': 0.347}                                                 |
| 31 | precision (macro)    | 0.666                                                                           |
| 32 | precision (micro)    | 0.935                                                                           |
| 33 | rates (population)   | {'false': 0.921, 'true': 0.079}                                                 |
| 34 | rates (sample)       | {'false': 0.926, 'true': 0.074}                                                 |
| 35 | recall (labels)      | {'false': 0.862, 'true': 0.855}                                                 |
| 36 | recall (macro)       | 0.858                                                                           |
| 37 | recall (micro)       | 0.861                                                                           |
| 38 | roc_auc (labels)     | {'false': 0.923, 'true': 0.922}                                                 |
| 39 | roc_auc (macro)      | 0.923                                                                           |
| 40 | roc_auc (micro)      | 0.923                                                                           |


Score schema of the 'reverted model':

**prediction**: 
description: 'The most likely label predicted by the estimator', 'type': 'boolean',
              
**probability**: 
'description': 'A mapping of probabilities onto each of the potential output labels',
              'properties': 'false': 'type': 'number', 'true': 'type': 'number'

**title**: 'Scikit learn-based classifier score with probability'

The API call https://ores.wikimedia.org/v3/scores/elwiki/807457197/reverted?features=true returns information about the models features it is looking at for making a prediction about an article revision.

The reverted model has  78  features. But most of them have the vlaue 0.
Number of features where the value is different from 0:  29

### Openness
...

### Intrinsic interpretability
...

### Algorithmic transparency
...

### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_
