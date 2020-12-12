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

### Openness
 * The model (code) and training/test data are publicly inspectable
 
  After some research, we did manage to find the model's repository (Edit Quality)[https://github.com/wikimedia/editquality].
  It contains datasets for different wikis and some information about the used models.
  We could not find the model's code and believe that it lies here (Revscoring)[https://github.com/wikimedia/revscoring].
  It seems, that the (Gradient Boosting Classifier)[https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html] of scikit-learn was used which uses regression trees. Regarding the training and test data, it is unclear to us how the provided data sets were used/split. In general, we were unable to find the code for building and training the model. On the positive side, there is a notebook that demonstrates how a model based on reversions could be build and that gives some insights about made decisions (note: it is only a demo).  https://github.com/wikimedia/editquality/blob/master/ipython/reverted_detection_demo.ipynb
  Overall it was quite difficult to find information about the models used and the corresponding test/training data. Not only were the repositories hard to find, their READMEs also did not provide a lot of information.
 
 * Individual decisions are reproducible 
 
 There are some tutorials on how to create feature lists and how to train models. These do not give many insights on how a specific model was built. As mentioned above, there is a demo (notebook) on how to build/train/test a model using revisions. Overall, the repositories' documentation is rather poor and it takes time to gather information looking through many files and code.
 
 * Changes are logged and version controlled
 
 Since GitHub is used to maintain the projects, changes are logged and one can revert to different versions of the project.
 

### Intrinsic interpretability
Intrinsic interpretability refers to models that are interpretable by themselves. It can be achieved, for example, through the imposition of constraints on the model. 


### Algorithmic transparency
 * Transparency applies at the level of the learning algorithm itself. 
 * Example: Understand the error metrics in linear regression


### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_
