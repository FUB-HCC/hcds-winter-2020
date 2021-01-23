# Title of your pos
> **Name:** `mane` Marisa N.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection

The guidlines infrom me about what I need to consider, when I want to design an interface for an AI system. The guidelines contain recommendations about which infromation should be made available, how an interaction between the system and the user should be made possible and how time factors should be taken into account. The additional examples help to understand how to practically apply these rules.


Question:

1. Should these guidelines not also apply for non-AI systems (i.e. for all decison-making or decison-supporting systems)?

I think that with AI systems there is a greater need for more specific design guidline for such systems. These systems become more and more complex and thus need better interfaces. But also non-AI systems can be complex and not transparent for the end-users. So I think these guidelines should be applicable for other applications. 


## A6 - Guidelines for Human-AI interaction


### 2 - Getting to know the context


**1. What is the COMPAS dataset about? Describe the COMPAS dataset.**

There is not just one COMPAS dataset but several different CSV files and even a DB file whithin the GitHub repository. ProRepublica states the file [compas-scores-raw.csv](https://github.com/propublica/compas-analysis/blob/master/compas-scores-raw.csv) to be the original COMPAS data. As ProRepublica mentions, this data was obtained through a public records request and contains two years of COMPAS scores from the Broward County Sheriff’s Office in Florida. This dataset has for all 18,610 people who were scored in 2013 and 2014 infromation about features which were also used by the COMPAS algorithm in scoring defendants. These featres include for example the age, sex, race, legal status or marital status of this person.

As noted by ProRepublica, *"because Broward County primarily uses the score to determine whether to release or detain a defendant before his or her trial"*, they discarded scores that were assessed at parole, probation or other stages in the criminal justice system from the original file. This resulted in the dataset [compas-scores.csv](https://github.com/propublica/compas-analysis/blob/master/compas-scores.csv) with 11,757 people who were assessed at the pretrial stage. This set is extended with the defendants outcomes within 2 years of the decision, meaning ProRebublica added information if a person was charged with new crimes over the next two years. 

Two more subsets of the data are provided, including a subset of only [violent recividism](https://github.com/propublica/compas-analysis/blob/master/compas-scores-two-years-violent.csv).

**2. What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on "Machine Bias"[2] and focus on the following table.**

ProRepublica found significant racial disparities. Eventhough the algoritm made mistakes in forecasting who would re-offend at roughly the same rate for both black and white defendants, the errors ad hand were very differently situated. *"The formula was particularly likely to falsely flag black defendants as future criminals, wrongly labeling them this way at almost twice the rate as white defendants"*. Whereas *"white defendants were mislabeled as low risk more often than black defendants"*.
    

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
