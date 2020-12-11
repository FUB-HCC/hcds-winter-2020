# Title of your post
> **Name:** `ansa` Anil S.
> **Session:** [05 Exercise - Transparency](https://github.com/FUB-HCC/hcds-winter-2020/wiki/05_exercise)   
----

## R5 - Reflection
> **Date:** DD.MM.YYYY - HH:MM PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> **Book:** "Interpretable machine learning. A Guide for Making Black Box Models Explainable" by Molnar

### 🗨️&nbsp; "How does the reading inform your understanding of human-centered data science?"  
_Answer in at least 2-3 complete sentences_

The article gives an overview of the taxonomy of interpretability methods.

The criteria are:
1. intrinsic or post hoc?
1. result of the interpretation method
1. Model-specific or model-agnostic?
1. local or global?

Each criteria lists classes of interpretation. This can be viewed as a little checklist to see how a model classifys in terms of interpretability.
This is crucial for a human-centred design perspective because to use a model wise we have to understand it. Which also means we have to interpret it.



### ❓&nbsp; Questions
1. Can we solve complex problems with only intrinsic machine models?

**Why:** Since we restrict the complexity of the model I asked myself if we can solve complex problems where maybe complex models are better suited.

***

## A4 - Transparency
> **Date:** DD.MM.YYYY - HH:MM PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> Group: ansa and mane <br>
> Model: damaging<br>

### Summary

_Please summarize your findings and analyses regarding (1) general understanding, (2) API, (3) ML algorithm and training/test data, and (4) features._

#### General Understanding

Getting a good understanding how this model is functioning and how it is integrated on a bigger scale inside the project is defenitely managable. Every article that is edited does go through this model and it decides wheter a edit is flagged as damaging or not. In case it is flagged as damaging the changes it made will be reverted.

#### API

The API was accessible and with feature injection we could gain more information about the model and the version currently running. Furthermore through the API we could see a little more into the model and if a certaing project is using this model. We can confidently say that API is an easy to access tool and it helped us to get a little more details. The problem we faced at the end of this phase was that we could not use the data without digging deeper in the algorithm. So there was data displayed but we could not really interpret it. That's where the next phase is playing role.

#### ML algorithm and training/test data 

Next, we focused on the actual ML model and the used training and test data. To first answer the question of which ML algorithm is used, we looked at the provided [API response](https://ores.wikimedia.org/v3/scores/enwiki?models=damaging&model_info). We were able to extract some information, for example, it is disclosed that **Gradient Boosting** is used as the main algorithm. Since we were not familiar with this term, we researched further and were able to find that this algorithm is only a generic term and uses other algorithms such as Regression for the classification task at hand. Even after further research, we could not find any information about which algorithm ORES actually uses Gradient Boosting. Furthermore, the API provides information about the used loss function (**Deviance**) and the criterion (**Friedman Mean Squared Error**). Unfortunately, it is not specified more precisely how these two functions are used. In ordinary ML architectures, the loss function and the criterion are often used as aliases. Mostly these functions describe the learing problem and need to be minimized or maximize in order to get a suitable model. We were not able to determine how exactly this both functions (**Deviance** and **Friedman Mean Squared Error**) are used within the context of our model. In Addition, the API provides notes about the used scoring scheme. As far as we know, this tells us how the output of the **Gradient Boosting** algorithm is subsequently processed in order to deliver a probability distribution or make a prediction at the end of the model pipline. We were not able to check whether our assumptions were correct, since forther referneces were missing here as well.

Next, we focused at the information about the model performance. Therefore, we took a closer look at the metrics provided by the API, which contain information about various aspects, such as general statistics like the size of the test set and the distribution of the labels, as well as standard performance measurements, such as a **Confusion Matrix** (true positive, true negative, etc. values), **Precision** and **Recall**. Unfortunately, it was not clear how the **Confusion Matrix** is to be understood, e.g. what the true positive, etc. values represents. Questions also arise with the other metrics, as there are no more precise descriptions of them, only keywords that are not always unambiguous, such as **!precision**, which could mean negative precision, i.e. negative predictive value. There are also two values **micro** and **macro** for each metric. After research, we were able to find out what these stand for, but not how these algorithms were acctualy applied to the test data set. In addition, two further values are offered per metric (**label->false** and **lable->true**). We could not find any information on the meaning of these values, nor were we able to interpret them ourselves. Finally, it can be said, that depending on the respective metric, the model works in some cases quite good and in other cases rather poor, i.e. depending on the application, it must be decided which metric is most meaningful and whether the model should be used for this case or not.

Finally, the training and test data were subjected to a closer examination. For this, the ORES documentation was helpful, which informed us that the used training data for the damaging model was manually labeld by editors and/or volunteers of the specific wiki community. We also checked some other references such as the MetaWiki documentation about ORES of the [damaging model](https://meta.wikimedia.org/wiki/Objective_Revision_Evaluation_Service/damaging), the [Wiki labels documentation](https://meta.wikimedia.org/wiki/Wiki_labels) (Wiki labels is a tool/service/gadget which is used by ORES to manage projects in which editors are invited to label data) and the Wiki label project [Edit quality](https://en.wikipedia.org/wiki/Wikipedia:Labels/Edit_quality). All in all, it was noticed that there are several, relatively unstructured documentation pages, some of which contain duplicate information but, for example, no reference to the actual data. It could be determined in which process the data was generated, but not specifically by whom and what the result looked like. Furthermore, we used the previously mentioned statistics regarding the data set (e.g. the size of the test data set, etc.) to get a better picture.


#### Features

We also took a closer look at the API response in the context of the used features. In total, we were able to identify 78 different features that the model uses. For some features it was easy to guess - using the provided feature-key-names and feature-values - what they were about. For exapmle 'feature.revision.user.is_anon' is probably a boolean flag, which describes if the user who did this revision was an anonymous user or not. Other features are not very self-explanatory like 'feature.english.informals.revision.diff.match_prop_delta_sum' and we were not able to find any further information regarding this topic. 

Regarding the question about the most important feature, we were initially convinced that we could find a good answer using feature injection. But after a few attempts we found out that it is not as easy as we thought. For example one attempt was to change each feature value seperately and then measure the resulting predictet probability distribution. We then compared the differences between these probability distributions and the baseline probability (the probability without changing any feature value) with the jensen shannon dinstance. But the problem was that the model always uses all features. So when we set a value to 0, change a value from 0 to 100 or set a False value to True, these changes can not be comapred. To be able to really compare the outputs, we need to be able to exclude features from the prediction completely, but this is not possible so far. 

All in all we can summarise that these features are not very well explained. We can guess the meaning of some of them but we can not be sure if this is the correct interpretation and how important these features really are for the prediction. Nevertheless, it is good to have at least a raw summary about which features are used and what values these features have for particular revisions.


### Openness

Regarding the openness of the damaging model, neither the actual code nor the data seems to be publicly accessible and thus there is no version control for either. Only a version number for the model indicates whether the model has changed or not. However, it cannot be clarified what the exact change is. Since this information is missing, it is also not possible to discuss individual decisions, because the decisions themselves are not disclosed or at least only very sparsely, such as the information about the main algorithm or the process of data collection. However, the provided information would have to be much more detailed and specific for each individual model in order to be able to reproduce the individual decisions. In the context of openness, we can summarize, that the model has major gaps and a lots of infromation needs to be opend up to the public in order to facilitate access to the key aspect of the model.


### Intrinsic interpretability

On the subject of intrinsic interpretability, it can be said that the main algorithm is known and is to a certain extent intrinsically interpretable (the algorithm works according to a kind of collective intelligence: many models that would not perform very well on their own deliver a good result together). But the problem is that it was not disclosed which algorithm gradient boosting uses. Therefore, one cannot draw any conclusions about the intrinsic interpretability of the model. So here, too, there are key aspects that needs to be improved.


### Algorithmic transparency

What can be said about the algorithmic transparency of the model is, that the actual algorithm is not visible and thus no transarency is given. On the positive side, however, metrics are made available that provide information on how well the algorithm works. Information on the data, how it was obtained, also contributes to better algorithmic transparency, but on the other hand the data is not visible and the metrics are partly not explained enough. Furthermore, although it can be positively emphasised that the use of a spicific model is communicated transparently when using the API, it is questionable whether this information is also passed on by the applications that use ORES to the people involved or affected. 


### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_

All in all the general understanding of the machine model was quite accessible. There was not a page exclusively for the damaging model which would defenitely increase the interpretability of the machine model. But still the information regarding the model was not hidden either. With a little engagement it was doable to get a general understanding. Now for our definition for transparency this model does not fullfill our criterias. Furthermore it lacks in all parts in our definition. That's why we would say this model fails in transparency.

Our advice to enhace transparency would be to create a seperate wikipage for the damaging model and to elaborate on the function of the model inside the wikimedia project. For the algorithmic transparency they could link a github repository where they could give us the model algorithm and the training and test data. In best case the repository should follow our reproducible workflow framework with a good README which explains the model even further. An important step also would be that they state hows they got the training and test data.
