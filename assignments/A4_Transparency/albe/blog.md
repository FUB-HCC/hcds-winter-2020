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

It is also mentioned that for intrinsically interpretable models the models internals (e.g. the learned weights) are inspected and tried to be explained. So do I got it right? Is the a criteria for an interpretation method to be characterized as *Intrinsic* that it is used for models with simple complexity and where the models internals are viewed?

**Why:** ...
I am asking this because I understand that per this definition Convolutional Neural Networks falls also to the *Intrinstic* interpretable models because of its learned weights and biases. But when I am thinking of some deep CNN's I cannot imagine these to be less complex.y.  

***

## A4 - Transparency
> **Date:** DD.MM.YYYY - HH:MM PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> Group: PERSON1 and PERSON2<br>
> Model: NAME OF MODEL<br>

### Summary 

_Please summarize your findings and analyses regarding (1) general understanding, (2) API, (3) ML algorithm and training/test data, and (4) features._


### (1) general understanding



###  ORES API (v3) 

Our exploration of the API showed us that it provides a lot of information about the different Wikipedia projects and the available models. 
It provides information on availability of a given model for different Wikipedia projects and exposes various information about the models.

Despite some some issues regarding the documentation we describe in the *openness* section below we belive the API offers information which are useful for the interpretability and the reproducibility of the model. 
<br>
In the following we are showing some of the insights were able to gather using the API. 

#### Model and project availability overview

With the help of the API call `https://ores.wikimedia.org/v3/scores/` we were able to find out in which projects our model is available in which version: 

<details>
  <summary>Table: Model availability overview</summary>

| model    | project      | version   |
|:---------|:-------------|:----------|
| reverted | bnwiki       | 0.5.0     |
| reverted | elwiki       | 0.5.0     |
| reverted | enwiktionary | 0.5.0     |
| reverted | glwiki       | 0.5.0     |
| reverted | hrwiki       | 0.5.0     |
| reverted | idwiki       | 0.5.0     |
| reverted | iswiki       | 0.5.0     |
| reverted | tawiki       | 0.5.0     |
| reverted | testwiki     | 0.0.3     |
| reverted | viwiki       | 0.5.0     |
| reverted | bnwiki       | 0.5.0     |
| reverted | elwiki       | 0.5.0     |
| reverted | enwiktionary | 0.5.0     |
| reverted | glwiki       | 0.5.0     |
| reverted | hrwiki       | 0.5.0     |
| reverted | idwiki       | 0.5.0     |
| reverted | iswiki       | 0.5.0     |
| reverted | tawiki       | 0.5.0     |
| reverted | testwiki     | 0.0.3     |
| reverted | viwiki       | 0.5.0     |

</details>

#### Model information

With the following two API calls it is possible to gather information on properties of a model like the *parameters* used for the model<br> 
<br>
`https://ores.wikimedia.org/v3/scores/enwiki?models=YOURMODELNAME&model_info`<br>
`https://ores.wikimedia.org/v3/scores/enwiki/REVID/YOURMODELNAME?model_info`<br>
<br>

On the following table we summarized for each property (column) which information is available for a model in detail. 
It is notable that aside of performace metrics model parameters such as the used loss function, learning rate etc. also 
detailed environment and system information is provided. We belive this are useful information for the reproducablity and also 
helps for the interpretablity. 


<details>
  <summary>Table: Model information overview</summary>
    

| params                   | environment           | statistics   | score_schema   |
|:-------------------------|:----------------------|:-------------|:---------------|
| ccp_alpha                | machine               | !f1          | properties     |
| center                   | platform              | !precision   | title          |
| criterion                | processor             | !recall      | type           |
| init                     | python_branch         | accuracy     |                |
| label_weights            | python_build          | counts       |                |
| labels                   | python_compiler       | f1           |                |
| learning_rate            | python_implementation | filter_rate  |                |
| loss                     | python_revision       | fpr          |                |
| max_depth                | python_version        | match_rate   |                |
| max_features             | release               | pr_auc       |                |
| max_leaf_nodes           | revscoring_version    | precision    |                |
| min_impurity_decrease    | system                | rates        |                |
| min_impurity_split       | version               | recall       |                |
| min_samples_leaf         |                       | roc_auc      |                |
| min_samples_split        |                       |              |                |
| min_weight_fraction_leaf |                       |              |                |
| multilabel               |                       |              |                |
| n_estimators             |                       |              |                |
| n_iter_no_change         |                       |              |                |
| population_rates         |                       |              |                |
| presort                  |                       |              |                |
| random_state             |                       |              |                |
| scale                    |                       |              |                |
| subsample                |                       |              |                |
| tol                      |                       |              |                |
| validation_fraction      |                       |              |                |
| verbose                  |                       |              |                |
| warm_start               |                       |              |                |

</details>

Here is an overview about the parameters of the model "reverted" for the wikipedia project "hrwiki":

<details>
  <summary>Table: Reverted model parameters</summary>

| param                    | value         |
|:-------------------------|:--------------|
| ccp_alpha                | 0.0           |
| center                   | 1.0           |
| criterion                | friedman_mse  |
| init                     |               |
| label_weights            | {'false': 10} |
| labels                   | [True, False] |
| learning_rate            | 0.01          |
| loss                     | deviance      |
| max_depth                | 3             |
| max_features             | log2          |
| max_leaf_nodes           |               |
| min_impurity_decrease    | 0.0           |
| min_impurity_split       |               |
| min_samples_leaf         | 5             |
| min_samples_split        | 2             |
| min_weight_fraction_leaf | 0.0           |
| multilabel               | False         |
| n_estimators             | 500           |
| n_iter_no_change         |               |
| population_rates         |               |
| presort                  | deprecated    |
| random_state             |               |
| scale                    | True          |
| subsample                | 1.0           |
| tol                      | 0.0001        |
| validation_fraction      | 0.1           |
| verbose                  | 0             |
| warm_start               | False         |

</details>


<details>
  <summary>Table: Reverted model environment properties</summary>

| environment property   | value                                        |
|:-----------------------|:---------------------------------------------|
| machine                | x86_64                                       |
| platform               | Linux-4.9.0-11-amd64-x86_64-with-debian-9.12 |
| processor              |                                              |
| python_branch          |                                              |
| python_build           | ['default', 'Sep 27 2018 17:25:39']          |
| python_compiler        | GCC 6.3.0 20170516                           |
| python_implementation  | CPython                                      |
| python_revision        |                                              |
| python_version         | 3.5.3                                        |
| release                | 4.9.0-11-amd64                               |
| revscoring_version     | 2.8.0                                        |
| system                 | Linux                                        |
| version                | #1 SMP Debian 4.9.189-3+deb9u1 (2019-09-20)  |

</details>

We checked if the stats are realy the same as the general modelinfo API call provides for the reverted model. We can confirm that it does provide consistent information.

<details>
  <summary>Table: Reverted model performance metrics</summary>

| metrics              | value                                                                           |
|:---------------------|:--------------------------------------------------------------------------------|
| !f1 (labels)         | {'false': 0.494, 'true': 0.919}                                                 |
| !f1 (macro)          | 0.707                                                                           |
| !f1 (micro)          | 0.527                                                                           |
| !precision (labels)  | {'false': 0.347, 'true': 0.986}                                                 |
| !precision (macro)   | 0.666                                                                           |
| !precision (micro)   | 0.398                                                                           |
| !recall (labels)     | {'false': 0.855, 'true': 0.862}                                                 |
| !recall (macro)      | 0.858                                                                           |
| !recall (micro)      | 0.855                                                                           |
| accuracy (labels)    | {'false': 0.861, 'true': 0.861}                                                 |
| accuracy (macro)     | 0.861                                                                           |
| accuracy (micro)     | 0.861                                                                           |
| counts (labels)      | {'false': 18232, 'true': 1452}                                                  |
| counts (n)           | 19684                                                                           |
| counts (predictions) | {'false': {'false': 15708, 'true': 2524}, 'true': {'false': 211, 'true': 1241}} |
| f1 (labels)          | {'false': 0.919, 'true': 0.494}                                                 |
| f1 (macro)           | 0.707                                                                           |
| f1 (micro)           | 0.886                                                                           |
| filter_rate (labels) | {'false': 0.195, 'true': 0.805}                                                 |
| filter_rate (macro)  | 0.5                                                                             |
| filter_rate (micro)  | 0.244                                                                           |
| fpr (labels)         | {'false': 0.145, 'true': 0.138}                                                 |
| fpr (macro)          | 0.142                                                                           |
| fpr (micro)          | 0.145                                                                           |
| match_rate (labels)  | {'false': 0.805, 'true': 0.195}                                                 |
| match_rate (macro)   | 0.5                                                                             |
| match_rate (micro)   | 0.756                                                                           |
| pr_auc (labels)      | {'false': 0.992, 'true': 0.527}                                                 |
| pr_auc (macro)       | 0.76                                                                            |
| pr_auc (micro)       | 0.956                                                                           |
| precision (labels)   | {'false': 0.986, 'true': 0.347}                                                 |
| precision (macro)    | 0.666                                                                           |
| precision (micro)    | 0.935                                                                           |
| rates (population)   | {'false': 0.921, 'true': 0.079}                                                 |
| rates (sample)       | {'false': 0.926, 'true': 0.074}                                                 |
| recall (labels)      | {'false': 0.862, 'true': 0.855}                                                 |
| recall (macro)       | 0.858                                                                           |
| recall (micro)       | 0.861                                                                           |
| roc_auc (labels)     | {'false': 0.923, 'true': 0.922}                                                 |
| roc_auc (macro)      | 0.923                                                                           |
| roc_auc (micro)      | 0.923                                                                           |

</details>

Score schema of the 'reverted model':

<details>
  <summary>Reverted model score schema</summary>

**prediction**: 
description: The most likely label predicted by the estimator, type: boolean<br>
              
**probability**: 
description: A mapping of probabilities onto each of the potential output labels<br>
             properties: 'false': 'type': 'number', 'true': 'type': 'number'<br>

**title**: Scikit learn-based classifier score with probability

</details>

<details>
  <summary>Reverted model all freatures</summary>

|---:|:---------------------------------------------------------------------|----------------:|
|  0 | feature.croatian.badwords.revision.diff.match_delta_decrease         |     0           |
|  1 | feature.croatian.badwords.revision.diff.match_delta_increase         |     0           |
|  2 | feature.croatian.badwords.revision.diff.match_delta_sum              |     0           |
|  3 | feature.croatian.badwords.revision.diff.match_prop_delta_decrease    |     0           |
|  4 | feature.croatian.badwords.revision.diff.match_prop_delta_increase    |     0           |
|  5 | feature.croatian.badwords.revision.diff.match_prop_delta_sum         |     0           |
|  6 | feature.croatian.informals.revision.diff.match_delta_decrease        |     0           |
|  7 | feature.croatian.informals.revision.diff.match_delta_increase        |     0           |
|  8 | feature.croatian.informals.revision.diff.match_delta_sum             |     0           |
|  9 | feature.croatian.informals.revision.diff.match_prop_delta_decrease   |     0           |
| 10 | feature.croatian.informals.revision.diff.match_prop_delta_increase   |     0           |
| 11 | feature.croatian.informals.revision.diff.match_prop_delta_sum        |     0           |
| 12 | feature.english.badwords.revision.diff.match_delta_decrease          |     0           |
| 13 | feature.english.badwords.revision.diff.match_delta_increase          |     0           |
| 14 | feature.english.badwords.revision.diff.match_delta_sum               |     0           |
| 15 | feature.english.badwords.revision.diff.match_prop_delta_decrease     |     0           |
| 16 | feature.english.badwords.revision.diff.match_prop_delta_increase     |     0           |
| 17 | feature.english.badwords.revision.diff.match_prop_delta_sum          |     0           |
| 18 | feature.english.informals.revision.diff.match_delta_decrease         |     0           |
| 19 | feature.english.informals.revision.diff.match_delta_increase         |     0           |
| 20 | feature.english.informals.revision.diff.match_delta_sum              |     0           |
| 21 | feature.english.informals.revision.diff.match_prop_delta_decrease    |     0           |
| 22 | feature.english.informals.revision.diff.match_prop_delta_increase    |     0           |
| 23 | feature.english.informals.revision.diff.match_prop_delta_sum         |     0           |
| 24 | feature.len(<datasource.tokenized(datasource.revision.parent.text)>) |  9877           |
| 25 | feature.len(<datasource.tokenized(datasource.revision.text)>)        |  9902           |
| 26 | feature.len(<datasource.wikitext.revision.markups>)                  |  3384           |
| 27 | feature.len(<datasource.wikitext.revision.parent.markups>)           |  3380           |
| 28 | feature.len(<datasource.wikitext.revision.parent.uppercase_words>)   |    46           |
| 29 | feature.len(<datasource.wikitext.revision.parent.words>)             |  2083           |
| 30 | feature.len(<datasource.wikitext.revision.words>)                    |  2089           |
| 31 | feature.revision.comment.has_link                                    |     0           |
| 32 | feature.revision.comment.suggests_section_edit                       |     1           |
| 33 | feature.revision.diff.longest_new_repeated_char                      |     1           |
| 34 | feature.revision.diff.longest_new_token                              |     1           |
| 35 | feature.revision.page.is_articleish                                  |     0           |
| 36 | feature.revision.page.is_draftspace                                  |     0           |
| 37 | feature.revision.page.is_mainspace                                   |     0           |
| 38 | feature.revision.user.has_advanced_rights                            |     0           |
| 39 | feature.revision.user.is_admin                                       |     0           |
| 40 | feature.revision.user.is_anon                                        |     0           |
| 41 | feature.revision.user.is_bot                                         |     0           |
| 42 | feature.revision.user.is_curator                                     |     0           |
| 43 | feature.revision.user.is_patroller                                   |     0           |
| 44 | feature.revision.user.is_trusted                                     |     0           |
| 45 | feature.temporal.revision.user.seconds_since_registration            |     4.62928e+08 |
| 46 | feature.wikitext.revision.chars                                      | 27321           |
| 47 | feature.wikitext.revision.diff.markup_delta_decrease                 |     0           |
| 48 | feature.wikitext.revision.diff.markup_delta_increase                 |     4           |
| 49 | feature.wikitext.revision.diff.markup_delta_sum                      |     4           |
| 50 | feature.wikitext.revision.diff.markup_prop_delta_decrease            |     0           |
| 51 | feature.wikitext.revision.diff.markup_prop_delta_increase            |     0.0036065   |
| 52 | feature.wikitext.revision.diff.markup_prop_delta_sum                 |     0.0036065   |
| 53 | feature.wikitext.revision.diff.number_delta_decrease                 |     0           |
| 54 | feature.wikitext.revision.diff.number_delta_increase                 |     1           |
| 55 | feature.wikitext.revision.diff.number_delta_sum                      |     1           |
| 56 | feature.wikitext.revision.diff.number_prop_delta_decrease            |     0           |
| 57 | feature.wikitext.revision.diff.number_prop_delta_increase            |     0.5         |
| 58 | feature.wikitext.revision.diff.number_prop_delta_sum                 |     0.5         |
| 59 | feature.wikitext.revision.diff.uppercase_word_delta_decrease         |     0           |
| 60 | feature.wikitext.revision.diff.uppercase_word_delta_increase         |     0           |
| 61 | feature.wikitext.revision.diff.uppercase_word_delta_sum              |     0           |
| 62 | feature.wikitext.revision.diff.uppercase_word_prop_delta_decrease    |     0           |
| 63 | feature.wikitext.revision.diff.uppercase_word_prop_delta_increase    |     0           |
| 64 | feature.wikitext.revision.diff.uppercase_word_prop_delta_sum         |     0           |
| 65 | feature.wikitext.revision.external_links                             |     0           |
| 66 | feature.wikitext.revision.headings                                   |    12           |
| 67 | feature.wikitext.revision.parent.chars                               | 27253           |
| 68 | feature.wikitext.revision.parent.external_links                      |     0           |
| 69 | feature.wikitext.revision.parent.headings                            |    12           |
| 70 | feature.wikitext.revision.parent.ref_tags                            |     0           |
| 71 | feature.wikitext.revision.parent.tags                                |   945           |
| 72 | feature.wikitext.revision.parent.templates                           |     7           |
| 73 | feature.wikitext.revision.parent.wikilinks                           |   830           |
| 74 | feature.wikitext.revision.ref_tags                                   |     0           |
| 75 | feature.wikitext.revision.tags                                       |   946           |
| 76 | feature.wikitext.revision.templates                                  |     7           |
| 77 | feature.wikitext.revision.wikilinks                                  |   831           |

 </details>

The API call https://ores.wikimedia.org/v3/scores/elwiki/807457197/reverted?features=true returns information about the models features it is looking at for making a prediction about an article revision.

The reverted model has  78  features. But most of them have the vlaue 0.
Number of features where the value is different from 0:  29



#### Feature injection: 

| injected feature                                               |   probability (false) |   probability (true) |   prediction |
|:---------------------------------------------------------------|----------------------:|---------------------:|-------------:|
| without feature injection                                      |              0.826583 |            0.173417  |            0 |
| user.is_bot=true                                               |              0.958514 |            0.0414857 |            0 |
| is_trusted=false                                               |              0.826583 |            0.173417  |            0 |
| feature.croatian.badwords.revision.diff.match_delta_increase=2 |              0.81254  |            0.18746   |            0 |
| feature.english.badwords.revision.diff.match_delta_increase=2  |              0.826583 |            0.173417  |            0 |


## (3) ML algorithm and training/test data, and (4) features._


### Openness
...

### Intrinsic interpretability
...

### Algorithmic transparency
...

### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_
