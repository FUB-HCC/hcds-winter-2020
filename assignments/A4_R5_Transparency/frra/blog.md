# Assignment 5 - Transparency 
> **Name:** `frra` Franziska R.
> **Session:** [05 Exercise - Transparency](https://github.com/FUB-HCC/hcds-winter-2020/wiki/05_exercise)   
----

## R5 - Reflection
> **Date:** 08.12.2020 - 01:00 PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> **Book:** "Interpretable machine learning. A Guide for Making Black Box Models Explainable" by Molnar

### 🗨️&nbsp; "How does the reading inform your understanding of human-centered data science?"  
This chapter is about how interpretability can be either achieved by restricting a models complexity (also referred to as "intrinsic") or by analyzing the model with certain methods after training (post-hoc). The first thing that came to my mind were Neural Networks. They are commonly used but sometimes way too complex to interpret. And it reminded me of a sentence "complex models are not always te best models". So reducing the complexity or using a simpler model can also achieve good results and in addition it is more interpretable. Due to the fact that not all models (or parameters e.g.) are accessible (black box) there is only the opportunity to analyse the model afterwards, by for example using summary statstics or looking at the used weights. 


### ❓&nbsp; Questions

1. Is there a "best practices" when trying to achieve good results but also model interpretability? 

***

## A5 - Transparency
> **Date:** 13.12.2020 - 15:00 PM *(Due: 08.12.2020 - 03:00 PM)*<br>
> Group: Franziska and Lukas<br>
> Model: draftquality<br>

### Summary 

The quality of articles is one of the most important things. To ensure that spam and vandalism do not affect the articles, the draftquality model can be used. Machine predictions can help curators focus on the most problematic new pages first. Based on comments left by admins when they delete pages, the model can be trained to predict which pages will need quick deletion.

Overall the model is a great tool, to automate the process of filtering out unwanted and potentially harmfull articles, that helps wikipedians when reviewing articles and increases the user experience in generall. 

The given API's are very usefull in providing information about the model and it's performance. The underlying ML algorithms and their performance are also displayed in detail, by showing different metrics on how well it's predictions work. 

In terms of features the provided API can be used to inspect all the features and their respectable values, meaning their significance when determining the overall quality of the article.



### Openness
1. the model (code) is publicly inspectable

  * The models code is publicly available on [Github](https://github.com/wikimedia/draftquality).

2. the training/test data are publicly inspectable

  * Looking at the folder [Datasets](https://github.com/wikimedia/draftquality/tree/master/datasets) in the github repository, we could find the data which is used. But we are not sure if it is used as training/test set, since no information are provided. Looking at all the API calls, they never contained any information of which data was used (except that labeled articles are used). 

3. individual decisions are reproducible

  * The documentation of the repository is rather poor, therefore it is hard to comprehent on how to reproduce the project. It is possible to download and use the model (or use the API for that), but if we would like to edit the code or something else it is hard to look trough all files and all the code. A more detailed documentation would help a lot. 

4. changes are logged and version controlled

  * Since github is used, the changes are all logged. In addition the versions are available, which can be also seen in our notebook from one of the API calls.

### Intrinsic interpretability
* Intrinsically interpretable models:
  * Models that are interpretable by design
  * No post-processing steps are needed to achieve interpretability

The Gradient Boosting algorithm with decision trees was used. The decision tree algorithm can be easily interpreted. Gradient Boosting produces a prediction model in the form of an ensemble of weak prediction models (in this case decision trees). It relies on the intuition that the best possible next model, when combined with previous models, minimizes the overall prediction error. These models can get quite complex, and it is questionable if it is intrinsicly interpretable. Since (again) there is no documentation available it is hard to interpret this intrinsically, for that we would have inspected the code in detail. 

### Algorithmic transparency
In terms of algorithmic transparency a lot of information are provided, as it can be seen in one of our API calls (model info). The results provided the information that scikit learn Gradient Boosting is used. Information of the scikit learn Gradient Boosting algorithm can be found on the website of [scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html). We could also figure out which parameters and values were used in the model. Another output are some statistical metrics which were used to evalute the models performance and results. They used many of the typical metrics for that. 

### Conclusion

Overall my group member and I think the project ORES and the related algorithms to maintain wikipedia are not only very usefull and functional, but also provide a good level of transparency. Besides some mentioned problems with missing documentation the amount of information about the model, the alogorithms it uses, and their performance gives a good insight of the models output and helps to identify potential points of failure. 

Also we were pleasantly surprised by the level of openness that the ORES provides. By having publically accessible training and test data, as well as model code, the ORES makes it reasonably easy to comprehend it's functionality.
