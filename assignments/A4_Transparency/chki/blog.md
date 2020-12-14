# Transparency
> **Name:** `chki` Christopher K.
> **Session:** [05 Exercise - Transparency](https://github.com/FUB-HCC/hcds-winter-2020/wiki/05_exercise)   
----

## R5 - Reflection
> **Date:** 03.12.2020 - 18:00 PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> **Book:** "Interpretable machine learning. A Guide for Making Black Box Models Explainable" by Molnar

### 🗨️&nbsp; "How does the reading inform your understanding of human-centered data science?"  
_Answer in at least 2-3 complete sentences_
Interpretability of a model can either be intrinsic (due to the simplicity of the model) or achieved post-hoc by applying certain methods.
There are model-specific methods/tools for model interpretation and model-agnostic tools. The former (usually based on the model's internals) are - as the name implies - specific to a model. The latter can theoretically be used on any machine learning model. They usually use the model's input-output-pairs and are applied post-hoc.

### ❓&nbsp; Questions
1. Can post-hoc methods ever achieve the degree of interpretability/transparency that intrinsic models offer?
1. With regard to the last question: I think that the necessary degree of interpretability depends on the use case. There might be cases in which simplistic models are too weak for modeling complex situations. So at some point, I assume, we are dependent on methods for interpretability. How do we assure high interpretability for complex models in sensitive application scenarios? Can these methods create enough transparency and trust?


***

## A4 - Transparency
> **Date:** 12.12.2020 - 03:00 PM *(Due: 14.12.2020 - 03:00 PM)*<br>
> Group: Ali B. and Christopher K.<br>
> Model: reverted<br>

### Summary 

_Please summarize your findings and analyses regarding (1) general understanding, (2) API, (3) ML algorithm and training/test data, and (4) features._

#### 1. General understanding

The _reverted_ model is part of ORES whis is an API that provides machine learning as a service for Wikimedia projects. The model predicts whether an edit to an article will eventually be reverted. It is used, for example, by quality control tools like [Edit Review Improvements (ERI)](https://www.mediawiki.org/wiki/Edit_Review_Improvements/New_filters_for_edit_review) and [Huggle](https://en.wikipedia.org/wiki/Wikipedia:Huggle). A list of tools can be found [here](https://www.mediawiki.org/wiki/ORES/Applications). The model can help reviewers find potentially damaging contributions and helps filtering through the Special:RecentChanges feed. That way the model aims to reduce the work of reviewers/editors and to increase their productivity.
The model is mainly used by editors/reviewers, developers (of third party tools, at the Wikimedia Foundation and Wikimedia Deutschland) but also by scientists.

_reverted_ is only available for very few projects: bnwiki, elwiki, enwiktionary, glwiki, hrwiki, idwiki, iswiki, tawiki, testwiki, viwiki.  

#### 2. ORES API (v3) 

Our exploration of the API showed us that it provides a lot of information about the different Wikipedia projects and the available models. 

It provides information on availability of a given model for different Wikipedia projects and exposes various information about the models.

Despite some issues about the documentation we describe in the *openness* section below we belive the API offers information which are useful for the interpretability and the reproducibility of the model. 
<br>

In the following we are showing some of the insights were able to gather using the API. 

#### Model and project availability overview

With the help of the API call `https://ores.wikimedia.org/v3/scores/` we were able to find out in which version our model is available in which project: 

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

With the following two API calls it is possible to gather various information like the used parameters, environment and performance metrics of the model.<br> 

<br>
`https://ores.wikimedia.org/v3/scores/enwiki?models=YOURMODELNAME&model_info`<br>
`https://ores.wikimedia.org/v3/scores/enwiki/REVID/YOURMODELNAME?model_info`<br>
<br>

On the following table we summarized columnwise for each property of the model which information is available in detail. 

It is notable that aside of performance metrics information a lot more information such as the model parameters, the used loss function, learning rate etc. as well as detailed about the environment and system information is provided. 

We consider this information to be useful for the reproducablity and belive that it is also helpful for the interpretablity of the model. 

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

In the following we show more detailed information about the various model properties.

Following is an overview about the parameters of the "reverted" model version 0.5.0:

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

The following table contains information about the environment used for training the `reverted` model version 0.5.0.

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

The following table has numerous performance measures for the reverted model version 0.5.0. Although we do not know all of these metrics we belive that many of them like the f1 score, the recall, precision and the confusion metrics is very useful information for judging and interpreting predictions of the model. 

By asking ourselves why the model information is available via two different API calls (1) where the model info for all models is returned (2) where a prediction for a revision id together with the modelinfo is returned we belive that the latter is available 

to inspect a prediction side by side with the used models information.

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

The modelinfo API call also provides a brief but in our opinion understandable description of the score which is returned by the model: 

<details>
  <summary>Reverted model score schema</summary>

**prediction**: 
description: The most likely label predicted by the estimator, type: boolean<br>
              
**probability**: 
description: A mapping of probabilities onto each of the potential output labels<br>
             properties: 'false': 'type': 'number', 'true': 'type': 'number'<br>

**title**: Scikit learn-based classifier score with probability

</details>


#### Model features:

The API call `https://ores.wikimedia.org/v3/scores/hrwiki/807457197/reverted?features=true` returns information about the models 

features and the activation values for these features for the specified revision id and project. 

In the section [model features](#model-features) we describe our understanding of these features and show our results with injecting some chosen features. 

<details>
  <summary>Reverted model all freatures</summary>

| feature                                                              |           value |
|:---------------------------------------------------------------------|----------------:|
| feature.croatian.badwords.revision.diff.match_delta_decrease         |     0           |
| feature.croatian.badwords.revision.diff.match_delta_increase         |     0           |
| feature.croatian.badwords.revision.diff.match_delta_sum              |     0           |
| feature.croatian.badwords.revision.diff.match_prop_delta_decrease    |     0           |
| feature.croatian.badwords.revision.diff.match_prop_delta_increase    |     0           |
| feature.croatian.badwords.revision.diff.match_prop_delta_sum         |     0           |
| feature.croatian.informals.revision.diff.match_delta_decrease        |     0           |
| feature.croatian.informals.revision.diff.match_delta_increase        |     0           |
| feature.croatian.informals.revision.diff.match_delta_sum             |     0           |
| feature.croatian.informals.revision.diff.match_prop_delta_decrease   |     0           |
| feature.croatian.informals.revision.diff.match_prop_delta_increase   |     0           |
| feature.croatian.informals.revision.diff.match_prop_delta_sum        |     0           |
| feature.english.badwords.revision.diff.match_delta_decrease          |     0           |
| feature.english.badwords.revision.diff.match_delta_increase          |     0           |
| feature.english.badwords.revision.diff.match_delta_sum               |     0           |
| feature.english.badwords.revision.diff.match_prop_delta_decrease     |     0           |
| feature.english.badwords.revision.diff.match_prop_delta_increase     |     0           |
| feature.english.badwords.revision.diff.match_prop_delta_sum          |     0           |
| feature.english.informals.revision.diff.match_delta_decrease         |     0           |
| feature.english.informals.revision.diff.match_delta_increase         |     0           |
| feature.english.informals.revision.diff.match_delta_sum              |     0           |
| feature.english.informals.revision.diff.match_prop_delta_decrease    |     0           |
| feature.english.informals.revision.diff.match_prop_delta_increase    |     0           |
| feature.english.informals.revision.diff.match_prop_delta_sum         |     0           |
| feature.len(datasource.tokenized(datasource.revision.parent.text))   |  9877           |
| feature.len(datasource.tokenized(datasource.revision.text))          |  9902           |
| feature.len(datasource.wikitext.revision.markups)                    |  3384           |
| feature.len(datasource.wikitext.revision.parent.markups)             |  3380           |
| feature.len(datasource.wikitext.revision.parent.uppercase_words)     |    46           |
| feature.len(datasource.wikitext.revision.parent.words)               |  2083           |
| feature.len(datasource.wikitext.revision.words)                      |  2089           |
| feature.revision.comment.has_link                                    |     0           |
| feature.revision.comment.suggests_section_edit                       |     1           |
| feature.revision.diff.longest_new_repeated_char                      |     1           |
| feature.revision.diff.longest_new_token                              |     1           |
| feature.revision.page.is_articleish                                  |     0           |
| feature.revision.page.is_draftspace                                  |     0           |
| feature.revision.page.is_mainspace                                   |     0           |
| feature.revision.user.has_advanced_rights                            |     0           |
| feature.revision.user.is_admin                                       |     0           |
| feature.revision.user.is_anon                                        |     0           |
| feature.revision.user.is_bot                                         |     0           |
| feature.revision.user.is_curator                                     |     0           |
| feature.revision.user.is_patroller                                   |     0           |
| feature.revision.user.is_trusted                                     |     0           |
| feature.temporal.revision.user.seconds_since_registration            |     4.62928e+08 |
| feature.wikitext.revision.chars                                      | 27321           |
| feature.wikitext.revision.diff.markup_delta_decrease                 |     0           |
| feature.wikitext.revision.diff.markup_delta_increase                 |     4           |
| feature.wikitext.revision.diff.markup_delta_sum                      |     4           |
| feature.wikitext.revision.diff.markup_prop_delta_decrease            |     0           |
| feature.wikitext.revision.diff.markup_prop_delta_increase            |     0.0036065   |
| feature.wikitext.revision.diff.markup_prop_delta_sum                 |     0.0036065   |
| feature.wikitext.revision.diff.number_delta_decrease                 |     0           |
| feature.wikitext.revision.diff.number_delta_increase                 |     1           |
| feature.wikitext.revision.diff.number_delta_sum                      |     1           |
| feature.wikitext.revision.diff.number_prop_delta_decrease            |     0           |
| feature.wikitext.revision.diff.number_prop_delta_increase            |     0.5         |
| feature.wikitext.revision.diff.number_prop_delta_sum                 |     0.5         |
| feature.wikitext.revision.diff.uppercase_word_delta_decrease         |     0           |

</details>

#### 3. ML algorithm and training/test data

For building the model a Gradient Boosting Classifier was used. Gradient boosting creates an ensemble learner by iteratively adding weak learners (in this case decision trees) to an ensemble. The only two exceptions are enwiktionary (a dictionary) which uses a RandomForest model and testwiki that uses RevIDScorer. In this assignment we focus on the Wikipedia projects for different languages which means that we exclude enwiktionary and testwiki. The training and test data for the different wikis is available on GitHub and is based on the history of edits (and reverted edits) from a wiki.
Using the API, one can retrieve information about the model and it's performance. We further discuss this information in chapter "Openness".

#### 4. Features

For the `reverted` model we found the above listed 78 features. We noticed that only around one-third of these features are have values different from zero. 

<details>
  <summary>Reverted model features where value is different from zero</summary>

| feature                                                              |           value |
|:---------------------------------------------------------------------|----------------:|
| feature.len(datasource.tokenized(datasource.revision.parent.text))   |  9877           |
| feature.len(datasource.tokenized(datasource.revision.text))          |  9902           |
| feature.len(datasource.wikitext.revision.markups)                    |  3384           |
| feature.len(datasource.wikitext.revision.parent.markups)             |  3380           |
| feature.len(datasource.wikitext.revision.parent.uppercase_words)     |    46           |
| feature.len(datasource.wikitext.revision.parent.words)               |  2083           |
| feature.len(datasource.wikitext.revision.words)                      |  2089           |
| feature.revision.comment.suggests_section_edit                       |     1           |
| feature.revision.diff.longest_new_repeated_char                      |     1           |
| feature.revision.diff.longest_new_token                              |     1           |
| feature.temporal.revision.user.seconds_since_registration            |     4.62928e+08 |
| feature.wikitext.revision.chars                                      | 27321           |
| feature.wikitext.revision.diff.markup_delta_increase                 |     4           |
| feature.wikitext.revision.diff.markup_delta_sum                      |     4           |
| feature.wikitext.revision.diff.markup_prop_delta_increase            |     0.0036065   |
| feature.wikitext.revision.diff.markup_prop_delta_sum                 |     0.0036065   |
| feature.wikitext.revision.diff.number_delta_increase                 |     1           |
| feature.wikitext.revision.diff.number_delta_sum                      |     1           |
| feature.wikitext.revision.diff.number_prop_delta_increase            |     0.5         |
| feature.wikitext.revision.diff.number_prop_delta_sum                 |     0.5         |
| feature.wikitext.revision.headings                                   |    12           |
| feature.wikitext.revision.parent.chars                               | 27253           |
| feature.wikitext.revision.parent.headings                            |    12           |
| feature.wikitext.revision.parent.tags                                |   945           |
| feature.wikitext.revision.parent.templates                           |     7           |
| feature.wikitext.revision.parent.wikilinks                           |   830           |
| feature.wikitext.revision.tags                                       |   946           |
| feature.wikitext.revision.templates                                  |     7           |
| feature.wikitext.revision.wikilinks                                  |   831           |

</details>

By trying to sort the features into groups we we abl to identify two groups of features. Features related to (1) **language** *english*/*articles native language* & **delta in increase/decrease of bad words** (2) *user* related features. 

<details>
    <summary>User related freatures:</summary>

feature.revision.user.has_advanced_rights<br>
feature.revision.user.is_admin<br>
feature.revision.user.is_anon<br>
feature.revision.user.is_bot<br>
feature.revision.user.is_curator<br>
feature.revision.user.is_patroller<br>
feature.revision.user.is_trusted<br>
feature.temporal.revision.user.seconds_since_registration<br>
feature.enwiki.revision.cite_templates<br>
</details>

<details>
    <summary>Bad words and language related:</summary>

feature.croatian.badwords.revision.diff.match_delta_decrease<br>
feature.croatian.badwords.revision.diff.match_delta_increase<br>
feature.croatian.badwords.revision.diff.match_delta_sum<br>
feature.croatian.badwords.revision.diff.match_prop_delta_decrease<br>
feature.croatian.badwords.revision.diff.match_prop_delta_increase<br>
feature.croatian.badwords.revision.diff.match_prop_delta_sum<br>

feature.english.badwords.revision.diff.match_delta_decrease<br>    
feature.english.badwords.revision.diff.match_delta_increase<br>    
feature.english.badwords.revision.diff.match_delta_sum<br>    
feature.english.badwords.revision.diff.match_prop_delta_decrease<br>
feature.english.badwords.revision.diff.match_prop_delta_increase<br>
feature.english.badwords.revision.diff.match_prop_delta_sum<br>  
</details>

We selected 4 features for injecting because we assumed these to have and impact on the prediction of the model. The table below lists the outcome of the feature injection for the revision id 5618117 in the hrwiki project. The first line *without feature injection* shows the prediction for this revision without a feature injected.


#### Feature injection: 


| injected feature                                               |   probability (false) |   probability (true) |   prediction |
|:---------------------------------------------------------------|----------------------:|---------------------:|-------------:|
| without feature injection                                      |              0.826583 |            0.173417  |            0 |
| user.is_bot=true                                               |              0.958514 |            0.0414857 |            0 |
| is_trusted=false                                               |              0.826583 |            0.173417  |            0 |
| feature.croatian.badwords.revision.diff.match_delta_increase=2 |              0.81254  |            0.18746   |            0 |
| feature.english.badwords.revision.diff.match_delta_increase=2  |              0.826583 |            0.173417  |            0 |

Very suprising for us was the change in the probabilities when injecting the feature `user.is_bot=true`. We interpret this change in the probability distribution for true\false probability as the the model is trusting the edit more if it was made from a bot. 

By looking on the results for features *bad words increase delta* for croatian and english language we noticed that for the original language of the article the prediction changes in the negative direction while by an increase of bad words in english language the probabilities stay the same (we tested also with different values). 
How ever we consider this test as a quick exploration and try out of the *feature injection* feature of the API. As we tested only with one revision we cannot make any conclusion about the impact of the features with the outcome of this test. 


### Openness
 * The model (code) and training/test data are publicly inspectable
 
  After some research, we did manage to find the model's repository [Edit Quality](https://github.com/wikimedia/editquality).
  It contains datasets for different wikis and some information about the used models.
  We could not find the model's code and believe that it lies here [Revscoring](https://github.com/wikimedia/revscoring).
  It seems, that the [Gradient Boosting Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html) of scikit-learn was used which uses regression trees. Regarding the training and test data, it is unclear to us how the provided data sets were used/split. In general, we were unable to find the code for building and training the model (although we believe it is openly available somewhere). On the positive side, there is a [notebook](https://github.com/wikimedia/editquality/blob/master/ipython/reverted_detection_demo.ipynb) that demonstrates how a model based on reversions could be build and that gives some insights about made decisions (note: it is only a demo).
  Overall it was quite difficult to find information about the models used and the corresponding test/training data. Not only were the repositories hard to find, their READMEs also did not provide a lot of information.
 
 * Individual decisions are reproducible 
 
 There are some tutorials on how to create feature lists and how to train models. These do not give many insights on how a specific model was built. As mentioned above, there is a demo (notebook) on how to build/train/test a model using reversions. Since the notebook is only a demo, it also does not show the code used for specific models but at least gives a good impression on how they were built. This makes it hard to judge and evaluate specific models. Overall, the repositories' documentation is rather poor and it takes time to gather information looking through many files and code.
 
 * Changes are logged and version controlled
 
 Since GitHub is used to maintain the projects, changes are logged and one can revert to different versions of the project.
 

### Intrinsic interpretability
* Intrinsic interpretability refers to models that are interpretable by themselves. It can be achieved, for example, through the imposition of constraints on the model. 

Gradient Boosting with decision trees was used. Simple decision trees are easy to interpret. An ensemble of simple decision trees is more complex and harder to interpret. Depending on the complexity the model migth still be instrinsically interpretable. However, the models use over one hundred trees and there are no visualizations (even for just a single example) available. Both these things make the model hard to interpret intrinsically.


### Algorithmic transparency
* Transparency applies at the level of the learning algorithm itself. This includes whether the used (error) metrics are understandable.

Once you know that scikit learn is used, you can look up important information from the documentation. The chosen parameters for the model are provided via the API (model_info).
For example, often 'deviance' is chosen as the loss function to be optimized. The documentation tells us 'deviance' refers to deviance (= logistic regression) for classification with probabilistic outputs. To measure the quality of a split many models used 'friedman_mse'. On the [scikit learn website](https://scikit-learn.org/stable/modules/ensemble.html#gradient-boosting) a lot of information and further references about Gradient Boosting Classifier can be found. 
Whether the metrics and the algorithm are well understood and relativley easy to understand is hard to judge. After getting an initial overview, the metrics to choose from (split criterion and loss function) seem relativley simple.

### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_

The developers and maintainers of ORES did a good job on making information, source code and data available in GitHub. But, there are a few issues: One the one hand, it takes some effort to find the right repositories since they are not referenced in overview articles ([like this](https://www.mediawiki.org/wiki/ORES)). On the other hand, the repositories themselves are not extensivly documented which makes it hard to orient and find useful information.

The API provides information about a model's Machine Learning algorithm, the chosen parameters and features as well as performance metrics. Unfortunately, a good documentation is missing here as well so the meaning of some metrics and features remains unclear. 

Overall, a lot of important information is provided but often in a way that it takes some time and effort for it to be really useful. Some information had to be searched for because it was not available or referenced in a wiki or repository. As an example, the description of the parameters for the machine learning model can be mentioned (which we consider as important). This has a negative impact on reproducibility and the overall transpareny. 

