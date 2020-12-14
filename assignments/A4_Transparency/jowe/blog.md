# Title of your post
> **Name:** `jowe` Jonas W.
> **Session:** [05 Exercise - Transparency](https://github.com/FUB-HCC/hcds-winter-2020/wiki/05_exercise)   
----

## R5 - Reflection
> **Date:** DD.MM.YYYY - HH:MM PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> **Book:** "Interpretable machine learning. A Guide for Making Black Box Models Explainable" by Molnar

### 🗨️&nbsp; "How does the reading inform your understanding of human-centered data science?"  
There are multiple ways to distinguish methods to achieve interpretability such as intrinsic/post hoc which states whether the model was restricted in complexity, which is suitable for simple models such as short decision trees or linear models, or the model was interpreted after the training. Other points are the different kind of results these methods produce, whether the interpretation method is specific to the model or usable on different kind of models (model-agnostic). The last difference brought up is the explenation of a specific prediction from the model or the whole model itself from the interpretation method.


### ❓&nbsp; Questions
1. How commonly used are these methods to achieve interpretability in actual research?

***

## A4 - Transparency
> **Date:** DD.MM.YYYY - HH:MM PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> Group: Jonas W. and Sebastian K.<br>
> Model: drafttopic<br>

### Summary 

#### (1) general understanding 
The drafttopic model is designed to route newly created articles based on their apparent topical nature to interested reviewers. This is useful, because one of the biggest difficulties with reviewing new articles is finding someone appropriate to do this task. Due to a a gigantic variety of topics on Wikipedia, reviewers have to be picked accordingly to their skills and knowlegde to judge notability, relevance, and accuracy of an article. 
The drafttopic model can be used by anyone due to the fact that it is open source. Most probably it is used mostly by data scientists as well as bots on wikipedia. Stakeholders are for example people that are releasing content on wikipedia, want to understand user activity on the website or provide a better service to the users.
This is equally useful for Wikipedia and users on the website, because by redirecting new articles to suitable reviewers, the overall quality of information is more likely to increase.
The model is used only within enwiki.

#### (2) API 
The API has several different API calls that give information about specific models. One can check where a model is being used (with its used version) and then analyse the use in those specific projects. Then more detailed information can be retrieved like environment of the model, used params, the score_schema and different statistics. The API also allows to check the data for specific revisions.

#### (3) ML algorithm and training/test data
The Gradiant Boosting algorithm was used which is known for providing good results. Even though Wikipedia states that their ORES source code as well as the training/test data is public, we could not find either in the linked Github repository, so the specifics of the data are unknown.
#### (4) features
We were unable to access the features used by the model as it is possible with the other models, so we have no information about the features used or their importance.
### Openness
While the machine learning algorithm and some important 'arguments' are visible through 'model_info', the code of the model itself as well as its data are, as far as we can tell, not provided. This makes the model not open at all, since no indivdual decisions are reproducible, nor are the changes logged and versions visible to the public.

### Intrinsic interpretability
Since Gradiant Boosting is a pretty complex algorithm and the features aren't actually visible as is the case with other ORES models, the Intrinsic Interpretability is poor.

### Algorithmic transparency
While the algorithm itself, as well as important factors are visible to the public, the problems stated above make the Algorithmic Transparency pretty lacking as well.

### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_

While ORES itself seems to be a great system with great results, it doesn't seem to be as open as possible for a foundation like Wikimedia. Especially when looking at our model, the information to be retrieved was severly lacking, which may be due to the fact that the drafttopic model seems to be one of the smaller, less used and less developed models of ORES. Still, the creators didn't follow the best practices to ensure creating a model as open as possible to the public eye. 
