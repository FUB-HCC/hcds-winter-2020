# Title of your pos
> **Name:** `ansa` Anil S.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection
**How does this reading inform your understanding of HCDS?**

AI is more or less a new field which means there is not much standardization and guidelines for creating interactive systems. A team from Microsoft researchers tackled this task and created a guideline for creating interactive systems. This guideline should not be viewed as a checklist rather it should be dealt with as a support for decision choices. They aimed to make the guideline actionable and at the UI level.

**By reflecting on your sentences, list at least one question that occurred in your mind while reading, and explain your motivation for asking this question.**

Why did the team from Microsoft choose not to develop a checklist ? 
Is it even convenient to create a checklist for interactive AI systems?

Motivation: 
There is a good book (The Checklist - Atul Gawande) where the author explains that checklists are a good tool to keep human errors in check. Especially in fields where errors made by humans are fatal like the construction of airplanes. It may not be that interactive AI systems are making mistakes on that level but actually every system can benefit from reducing errors.


## A6


### 2 - Getting to know the context


**1. What is the COMPAS dataset about? Describe the COMPAS dataset.**

There is not just one COMPAS dataset but several different CSV files and even a DB file whithin the GitHub repository. ProRepublica states the file [compas-scores-raw.csv](https://github.com/propublica/compas-analysis/blob/master/compas-scores-raw.csv) to be the original COMPAS data. As ProRepublica mentions, this data was obtained through a public records request and contains two years of COMPAS scores from the Broward County Sheriff’s Office in Florida. This dataset has for all 18,610 people who were scored in 2013 and 2014 infromation about features which were also used by the COMPAS algorithm in scoring defendants. These featres include for example the age, sex, race, legal status or marital status of this person.

As noted by ProRepublica, *"because Broward County primarily uses the score to determine whether to release or detain a defendant before his or her trial"*, they discarded scores that were assessed at parole, probation or other stages in the criminal justice system from the original file. This resulted in the dataset [compas-scores.csv](https://github.com/propublica/compas-analysis/blob/master/compas-scores.csv) with 11,757 people who were assessed at the pretrial stage. This set is extended with the defendants outcomes within 2 years of the decision, meaning ProRebublica added information if a person was charged with new crimes over the next two years. 

Two more subsets of the data are provided, including a subset of only [violent recividism](https://github.com/propublica/compas-analysis/blob/master/compas-scores-two-years-violent.csv).

**2. What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on "Machine Bias"[2] and focus on the following table.**


We also turned up significant racial disparities, just as Holder feared. In forecasting who would re-offend, the algorithm made mistakes with black and white defendants at roughly the same rate but in very different ways. The formula was particularly likely to falsely flag black defendants as future criminals, wrongly labeling them this way at almost twice the rate as white defendants. White defendants were mislabeled as low risk more often than black defendants.
    

### 3 - Understand the ProPublica analysis

**3. Please describe your thoughts (positive and negative), when first looking and exploring the tool. (3-4 sentences in a pro/contra table)**

| At the first sight, I do not understand much and I am feeling a bit overwhelmed.                              | The interactive data visualization catches the eye and encourages you to go on. |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| The amount of information and options are too much (it is hard to figure out where to begin with exploring).  | The interactive design let you explore the tool in a playful way.               |
| The data and its features are not well explained.                                                             |                                                                                 |
| There are little information and descriptions about how to use the tool and how to get specific outcomes.     |                                                                                 |
| The raw data is not accessible.                                                                               |                                                                                 |

**4. Note down (document) the steps you need to undertake in order to achieve a similar analysis result as ProPublica. (steps, bullet points)**


1. Select the tab "Performance & Fairness"
2. Select as "Ground Truth Feature" "recidivism_within_2_years"
3. Select as "Slice by" "race"
4. Leave all other values as given
5. Look at the "False Positives", "Fale Negatives" and "Accuracy" of the "African-American" and "Causasian" entries


Result: As you can see after following these steps, the prediction for african-american and causasian defendants have almost the same accuracy, but the false positive rate is much higher for african-americans, whereas the false negative rate is a lot higher for caucasians.
