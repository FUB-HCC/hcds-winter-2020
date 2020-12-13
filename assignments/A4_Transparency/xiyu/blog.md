# Reflection 5
> **Name:** `xiyu` Xin Y.
> **Session:** [05 Exercise - Transparency](https://github.com/FUB-HCC/hcds-winter-2020/wiki/05_exercise)   
----

## R5 - Reflection
> **Date:** 07.12.2020 - 11:47 AM *(Due: 08.12.2020 - 03:00 PM)*<br>
> **Book:** "Interpretable machine learning. A Guide for Making Black Box Models Explainable" by Molnar

### 🗨️&nbsp; "How does the reading inform your understanding of human-centered data science?"  
_Answer in at least 2-3 complete sentences_

Interpretability can be offered through different methods regarding different respects. And various interpretation methods can be categorized regarding to different criterien. 
Intrisic method for interpretation is normally model specific and is closely related to model features, where as post hoc methods is normally applied after model training and provides more flexibility. On the other hand, the various interpretation methods can also be differentiated according to their results. Some interpretation methods may share common features are related with one other. 

### ❓&nbsp; Questions
1. I am still a little bit confused on difference between explanations and interpretations. In the chapter 2.2 (or generally chapter 2), it seems that the author use them as synonyms. 
<br>**Why:** I have read some general papers on XAI which describes interpretability as intrinsic explanability, therefore, it seems that interpretability is subconcept of explanability. I am unsure how to clearly differentiate them apart from each other or they are actually the synonyms. 

1. Is there any difference between interpretability or interpretation methods for parametric and non-parametric learning models? <br>**Why:** This question is interesting for me because some interpretation methods are based on parametric statistics, and I am wondering if there is something we need to consider of when choose an interpretation method. 

***

## A4 - Transparency
> **Date:** 10.12.2020 - 20:09 PM *(Due: 14.12.2020 - 12:00 PM)*<br>
> Group 5: Xin and Gorgin<br>
> Model: `articlequality`<br>

### Summary 

_Please summarize your findings and analyses regarding (1) general understanding, (2) API, (3) ML algorithm and training/test data, and (4) features._

About _general understanding_: The path of learning started at an article of Wikimedia about [Ores](https://diff.wikimedia.org/2015/11/30/artificial-intelligence-x-ray-specs/) where there was an outdated [link to Ores](https://meta.wikimedia.org/wiki/Objective_Revision_Evaluation_Service), but there was the [up-to-date link](https://www.mediawiki.org/wiki/ORES) available. The style of writing is in a way so even non-technicals could follow, which is nice but also lacks in-depth explanation.
<br> For the _API usage_ we get then to the ["Ores homepage"](https://ores.wikimedia.org/) where the [documentation](https://ores.wikimedia.org/v3/), which is actually a swagger page with only brief comments. To analyze the API, we also call API data to see its parameters in details. We see general information like the models in each certain wikiproject, the possibility distribution across quality classifications and feature counts for each article with a unique revision id. <br> The API call and documentation doesn't say much about the _training/testing data_, but our research on google found out a paper regardinng thie ORES project which provides the data and indicates that the test/training splitting is based on a stratified random sampling. 
The model info also provides the detailed information on applied _ML algorithm_. However, due to lack of solid mathematics background, we can evaluate the algorithmic performance only based on evaluation metrics but not from its technical details. For example, we can hardly say something about its parameter tuning for model optimization. 
<br> Unfortunately, although the _features_ used in algorithm are listed in API call, but so far we haven't found enough information on why those features are extracted as well as what do they exactly mean. There are still some ambiguities on features. 

### Openness

We think the openness of the model is somehow well supported by following aspects: open datasource, open github repository where we can find all source codes regarding our model, information-details in published-paper with open access, variety of information provided on API. We think although some information is not documented well and appropriately, but the information can still be found by in depth online searchning. 

### Intrinsic interpretability

We can't say that the intrinsic interpretability is well supported here since the gradient boosting is an emsemble of decision tree and we are currently unclear about all technique details. Although the gradient boosting classifier is an emsemble technique of decision trees, we were unable to figure out how the different decision trees are combined together by viewing the given information. At least, we found the model doesn't satisfy intrinsic interpretability at this stage, at least for non-experts in machine learning.

### Algorithmic transparency

From our perspect of view we also think this model lacks sufficient algorithmic transparency. Algorithmic transparency describes whether the purpose, structure and underlying actions of the algorithms are visible to users. As we mentioned before, we somehow see the parameters used in the parameter setting in model details from API call, it still remains unclear why the parameters are settled to a specific value, and how the algorithm delivers such classification for a certain revid. 


### Conclusion
_From a human-centered perspective - what do you think about your model and ORES in general?_

We think the model and ORES is a nice progress in general towards human-centered data science since the Wikipedian team make their efforts visible to public through different open channels, and they also provide API with fulfilled information. But due to its compicated technical details, it is quite hard to convey the logics behind the model to users who are non-ML experts. We think the researchers are still working on finding a solution to increase the interpretability as well as explanability to make it more understandable for general public.  
