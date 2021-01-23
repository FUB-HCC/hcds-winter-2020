# Assignment 6
> **Name:** `frra` Franziska R.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection
1. Answer in at least 2-3 complete sentences the question "How does the reading inform your understanding of human-centered data science?".

The guidelines for Human-AI Interaction were developed to help practitioners design better user-facing AI-based systems. The guidelines cover a broad range of interactions, starting from when a user is initially introduced to an AI system and extending to continuous interactions, AI model updates and refinements, as well as managing AI failures. Considering all the guidelines in the designing process should make an AI-based system better understandable and easier to use for humans. 

2. Question

Although most of the rules are very understandable, some leave room for interpretation. Taking the rules "Match relevant social norms" or "Mitigate social biases" is something that is not easily to estimate. 

How can we ensure the correct social and cultural context? The same goes with social biases. This is more of a question of ethics and probably cannot be answered that easily. 

## A6 - Guidelines for Human-AI interaction

### 1) Preparation

1. Check out the section Resources and concepts below, if you want to know more about the 18 Human-AI Guidelines, What-if-tool (WIT), COMPAS (dataset), or heuristic evaluations. This is not mandatory, but it should help you, if you need some more information or if you are just very curious!
2. Please note: The reading reflection (R7) will help you with this assignment. Please do this first. It lays the foundation regarding understanding the 18 human-AI interaction guidelines.
3. Please open the COMPAS Demo ➡️ https://pair-code.github.io/what-if-tool/demos/compas.html. We will evaluate this UI.
4. Please have the 18 guidelines open (examples for each are provided in the appendix of the original paper[2]).


### 2) Getting to know the context

#### 2.1) What is the COMPAS dataset about? Describe the COMPAS dataset.

The COMPAS ("*Correctional Offender Management Profiling for Alternative Sanctions*") dataset is a tool used by judges and probation/parole officers to predict a criminals likelihood to re-offend. The dataset contains 14 features reaching from age, to fellony count, to race and gender. These categories are then again devided into numerical *(9)* and categorical *(5)* features. In addition information about the average, or most common values of a particular feature are included, as well as a few other related statistics (median, min, etc.). 


#### 2.2)What kind of unfairness did ProPublica found in their analysis?

The Probublica analysis found a bias against African American people. White people with a similar or even more criminal background were often times predicted to be less likely to offend again. This was disputed by the analysis multiple times through, where criminal indiviuals were tracked for 2 years after their sentencing. Various examples show that many white individuals, who were considered a low risk, reoffended. This can also be seen in the table, where white individuals are much more likely to be labeled low risk, but actually reoffend, while when being labeled high risk, their chances of not offending again a substantially lower. Therefor both statistics show around a 20 % advantage for white indiviuals, which means black people are wrongly evaluated as being almost twice to reoffend.

### 3) Understand the ProPublica analysis

#### 3.3) Please describe your thoughts (positive and negative), when first looking and exploring the tool.

| pro  |  contra |
|---|---|
| Provides really nice overview of all the features and the prediction probability for each datapoint.|Getting started with the tool was a bit confusing at the first glance. | |The overview of each feature offers a good first impression on how each feature is distributed, this makes it easier to understand which feature  could play a more important role in the prediction.| |  Getting started with the tool was a bit confusing at the first glance. | 
| It is possible to create a similar feature like the selected datapoint  | Not really intuitiv  |  
| Visual performance exploration is a nice feature which also makes it possible to to adjust cost ratio for optimization  | Some things weren't really well explained within the tool, for example what the axes of the plot mean and what the default for it is  | 

---

#### 3.4) Note down (document) the steps you need to undertake in order to achieve a similar analysis result as ProPublica.

* on the site, select the *Performance and Fairness* column
* as Ground Truth Feature select *recidivism_within_2_years*
* for Slice by select *race*
* now you are presented with a list of 6 ethnicities, out of which select *African-American* and *Caucasian*
* at last, compare the two confusion matrices, where the differences as discribed in 2.2 can clearly be seen
