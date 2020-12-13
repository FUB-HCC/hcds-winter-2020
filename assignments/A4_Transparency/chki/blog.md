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

1. General understanding

The _reverted_ model is part of ORES whis is an API that provides machine learning as a service for Wikimedia projects. The model predicts whether an edit to an article will eventually be reverted. It is used, for example, by quality control tools like [Edit Review Improvements (ERI)](https://www.mediawiki.org/wiki/Edit_Review_Improvements/New_filters_for_edit_review) and [Huggle](https://en.wikipedia.org/wiki/Wikipedia:Huggle). A list of tools can be found [here](https://www.mediawiki.org/wiki/ORES/Applications). The model can help reviewers find potentially damaging contributions and helps filtering through the Special:RecentChanges feed. That way the model aims to reduce the work of reviewers/editors and to increase their productivity.
The model is mainly used by editors/reviewers, developers (of third party tools, at the Wikimedia Foundation and Wikimedia Deutschland) but also by scientists.

_reverted_ is only available for very few projects: bnwiki, elwiki, enwiktionary, glwiki, hrwiki, idwiki, iswiki, tawiki, testwiki, viwiki.  

2. API


3. ML algorithm and training/test data

For building the model a Gradient Boosting Classifier was used. Gradient boosting creates an ensemble learner by iteratively adding weak learners (in this case decision trees) to an ensemble. The only two exceptions are enwiktionary (a dictionary) which uses a RandomForest model and testwiki that uses RevIDScorer. In this assignment we focus on the Wikipedia projects for different languages which means that we exclude enwiktionary and testwiki. The training and test data for the different wikis is available on GitHub and is based on the history of edits (and reverted edits) from a wiki.
Using the API, one can retrieve information about the model and it's performance. We further discuss this information in chapter "Openness".

4. Features


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

