# Title of your pos
> **Name:** `chki` Christopher K.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection
#### Please read page three of the paper Guidelines for Human-AI Interaction. I recommend reading the appendix of the paper and, if you have time, the full paper - this is optional.

_Answer in at least 2-3 complete sentences the question "How does the reading inform your understanding of human-centered data science?"._

Universal design guidelines should be complemented by more specific guidlines for the application/use case at hand. For example, specific guidelines are important for systems using AI as they may show unpredictable behaviour due to their nature. Using these guidelines, confusion could be prevented and better informed actions could be taken by the user. 

_List at least one question that occurred in your mind while reading, and explain your motivation for asking this question._

Guideline G5 says "Match relevant social norms". I stumbled across that guideline for a couple of reasons. It seemed pretty general and not strongly related to AI. A couple of questions arised: What social norms are important and how should they be taken into account (in my specific context)? Is there related work or a list to refer to? Does this lead into the direction of personalized user experiences (or at least different interfaces tailored to needs of certain user groups)?


## A6 - xxx

#### 2. Getting to know the context
1. What is the COMPAS dataset about? Describe the COMPAS dataset. **(3-4 sentences)**

The COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) dataset is used by an algorithm to get predictions for a criminal's future behaviour. For a criminal, the algorithm estimates the risk/likelihood of reoffending/recidivism. The predictions were used, for example, by judges.
The dataset contains primarily demographic data, like first and last name, sex, ethnicity and date of birth.

1. What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on ["Machine Bias"](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)<sup>[2]</sup> and focus on the following table. **(3-4 sentences)**
ProPublica found that the risk of recidivism was often predicted too high for black defendants. At the same time, the risk for white defendants was often predicted too low. ProPublica's analysis showed that "white defendants who re-offended within the next two years were mistakenly labeled low risk almost twice as often as black re-offenders" [Source: ProPublica](https://www.propublica.org/article/how-we-analyzed-the-compas-recidivism-algorithm).


#### 3. Understand the ProPublica analysis
3. Please describe your thoughts (positive and negative), when first looking and exploring the tool. (3-4 sentences in a pro/contra table)

| Pro | Con |
|-------|-------|
| There is an informational text on the left side of the screen which gives a short introduction to the interface and possible interactions | There is are many elements present on the page. It is not clear where to look at first. |
| There are buttons available that - when clicked - reveal further information about certain functionality | There are many menus and options which functions are not clear at first sight |

4. Note down (document) the steps you need to undertake in order to achieve a similar analysis result as ProPublica. (steps, bullet points)
* Get a dataset of criminals, their demographic data, information about recidivism within two years and the model's prediction about recidivism.
* Compare the predictions with the actual outcomes
* Investigate how strong the different attributes influence the predictions 
* Check for biases and further investigate attributes that have a huge impact on the prediction.
