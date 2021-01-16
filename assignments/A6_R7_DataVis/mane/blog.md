# Title of your pos
> **Name:** `mane` Marisa N.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection
...

## A6 - xxx


### 2 - Getting to know the context


**1. What is the COMPAS dataset about? Describe the COMPAS dataset.**

There is not just one COMPAS dataset but several different CSV files and even a DB file whithin the GitHub repository. ProRepublica states the file [compas-scores-raw.csv](https://github.com/propublica/compas-analysis/blob/master/compas-scores-raw.csv) to be the original COMPAS data. As ProRepublica mentions, this data was obtained through a public records request and contains two years of COMPAS scores from the Broward County Sheriff’s Office in Florida. This dataset has for all 18,610 people who were scored in 2013 and 2014 infromation about features which were also used by the COMPAS algorithm in scoring defendants. These featres include for example the age, sex, race, legal status or marital status of this person.

As noted by ProRepublica, *"because Broward County primarily uses the score to determine whether to release or detain a defendant before his or her trial"*, they discarded scores that were assessed at parole, probation or other stages in the criminal justice system from the original file. This resulted in the dataset [compas-scores.csv](https://github.com/propublica/compas-analysis/blob/master/compas-scores.csv) with 11,757 people who were assessed at the pretrial stage. This set is extended with the defendants outcomes within 2 years of the decision, meaning ProRebublica added information if a person was charged with new crimes over the next two years. 

Two more subsets of the data are provided, including a subset of only [violent recividism](https://github.com/propublica/compas-analysis/blob/master/compas-scores-two-years-violent.csv).

**2. What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on "Machine Bias"[2] and focus on the following table.**


We also turned up significant racial disparities, just as Holder feared. In forecasting who would re-offend, the algorithm made mistakes with black and white defendants at roughly the same rate but in very different ways. The formula was particularly likely to falsely flag black defendants as future criminals, wrongly labeling them this way at almost twice the rate as white defendants. White defendants were mislabeled as low risk more often than black defendants.
    

### 3 - Understand the ProPublica analysis

3. Please describe your thoughts (positive and negative), when first looking and exploring the tool. (3-4 sentences in a pro/contra table)

| At the first sight, I do not understand much and I am feeling a bit overwhelmed.                              | The interactive data visualization catches the eye and encourages you to go on. |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| The amount of information and options are too much (it is hard to figure out where to begin with exploring).  | The interactive design let you explore the tool in a playful way.               |
| The data and its features are not well explained.                                                             |                                                                                 |
| There are little information and descriptions about how to use the tool and how to get specific outcomes.     |                                                                                 |
| The raw data is not accessible.                                                                               |                                                                                 |

4. Note down (document) the steps you need to undertake in order to achieve a similar analysis result as ProPublica. (steps, bullet points)






















We obtained the risk scores assigned to more than 7,000 people arrested in Broward County, Florida, in 2013 and 2014 and checked to see how many were charged with new crimes over the next two years, the same benchmark used by the creators of the algorithm.


Northpointe’s core product is a set of scores derived from 137 questions that are either answered by defendants or pulled from criminal records. Race is not one of the questions

It assesses not just risk but also nearly two dozen so-called “criminogenic needs” that relate to the major theories of criminality, including “criminal personality,” “social isolation,” “substance abuse” and “residence/stability.” Defendants are ranked low, medium or high risk in each category.

**“Risk of Recidivism,”**

Features:

https://www.rdocumentation.org/packages/fairml/versions/0.3/topics/compas

age: a continuous variable containing the age (in years) of the person; 

COMPASS_determination: Klassifizierung von COMPAS

juv_fel_count: a continuous variable containing the number of juvenile felonies;

juv_misd_count: a continuous variable containing the number of juvenile misdemeanors;

juv_other_count: a continuous variable containing the number of prior juvenile convictions that are not considered either felonies or misdemeanors;

priors_count: a continuous variable containing the number of prior crimes committed;

race: a factor encoding the race of the person;

recidivism_within_2_years: a factor with two levels "Yes" and "No" (if the person has recidivated within two years);

sex: a factor with levels "Female" and "Male"

Datapoint ID: Id des Datenpunktes

Inference score: Abgeleiteter Score, ob hohes oder niedreiges Risiko besteht; Zwischen 0 und 1

Inference value: Abgeleiteter Wert, ob hohes oder niedreiges Risiko besteht; 0 oder 1

Inference label: Abgeleitetes Label, ob hohes oder niedreiges Risiko besteht; "Low Risk" oder "High risk"

Inference correct: Gibt an, ob abgeleiteter Wert korrekt war; "correct" oder "incorrect"

**3496** datapoints loaded

