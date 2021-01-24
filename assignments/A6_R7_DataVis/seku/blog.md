# Assignment 6
> **Name:** `seku` Sebastian K.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection
1.Answer in at least 2-3 complete sentences the question "How does the reading inform your understanding of human-centered data science?".
In the given text the autors propose 18 generally applicable design guidelines for human-AI interaction, which should help developing better interfaces for AI Systems. In detail, the text covers a broad range of topics, which should be taken into account, so that the developer has a higher chance to create a good interface. By also providing examples, these guidlines can be used as a tool to make an eady to use system.

2. By reflecting on your sentences, list at least one question that occurred in your mind while reading, and explain your motivation for asking this question.
As the guide is a good tool to develop new interfaces, is there a possibility to automate verification of specific rules to for example reduce the effect of bias which is given by manual tests?

## A6 - Guidelines for Human-AI interaction 
### Getting to know the context
1. What is the COMPAS dataset about? Describe the COMPAS dataset.
The COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) dataset is used to determine the recidivism of criminals. The dataset is manly used by judges and parole officers. It consists of 9 numerical features (e.g. age, misdemeanor or felony count) and 5 categorical features (e.g. race and sex). Additionally the set gives information about the maximum, minimum and median count for the numerical features as well as some similar information for categorical features.

2. What kind of unfairness did ProPublica found in their analysis?
ProPublica found, that the dataset has a bias in terms of race. Black defendants were often predicted to be at a higher risk of recidivism than they actually were. This could be proven based on a follow up study, where defendants has been tracked for the following 2 years. The analysis shows, that many black defendats, who got a prediction to recidivate did not recidivate in the end wheres on the other hand many white defendats, who got a low risk for recidivism actually did recidivate.

### Understand the ProPublica analysis
| pro  |  contra |
|---|---|
|Plots in the data view help to understand the data|The GUI is not particulary easy to use (not intuitive)|
|The tool has a good documentation|Description does not really help understanding the tool|
|The data plot has good filter settings to understand the given data||
