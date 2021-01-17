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


### 4 - Understand the ProPublica analysis


#### INITIALLY

**01 Make clear what the system can do.**
**Help the user understand what the AI system is capable of doing.**

The name of the tool gives a good hint for what this model can be used for. When opening the demo there is a small text box explaining shortly what this model can do. It is probably not explaining all functionalities but this is good it gives new users a summary of the most important features.



**02 Make clear how well the system can do what it can do.**
**Help the user understand how often the AI system may make mistakes.** 

After playing a little bit around you can get a good sense how to tweak things to understand how well this tool get do what it is promising but it is not really intuitve.

#### DURING INTERACTION

**03 Time services based on context.**
**Time when to act or interrupt based on the user’s current task and environment.**

**04 Show contextually relevant information.**
**Display information relevant to the user’s current task and environment.**

positive:
1. 'Create similarity feature' - highlighted
1. 'prediction' button is highlighted after tweaking a datapoint
1. different tabs for different tasks
1. Shows the features and values of selected datapoints
1. Shows a graph of all datapoints and their class
1. Showing a legend for classes

negatives:
1. Features tab table seems to cluttered no clear seperation
1. 

**05 Match relevant social norms.**
**Ensure the experience is delivered in a way that users would expect, given their social and cultural context.**

**06 Mitigate social biases.**
**Ensure the AI system’s language and behaviors do not reinforce undesirable and unfair stereotypes and biases.**

#### WHEN WRONG

**07 Support efficient invocation.**
**Make it easy to invoke or request the AI system’s services when needed.**

**08 Support efficient dismissal.**
**Make it easy to dismiss or ignore undesired AI system services.**

**09 Support efficient correction.**
**Make it easy to edit, refine, or recover when the AI system is wrong.**

**10 Scope services when in doubt.**
**Engage in disambiguation or gracefully degrade the AI system’s services when uncertain about a user’s goals.**

**11 Make clear why the system did what it did.**
**Enable the user to access an explanation of why the AI system behaved as it did.v

#### OVER TIME

**12 Remember recent interactions.**
**Maintain short-term memory and allow the user to make efficient references to that memory.**

**13 Learn from user behavior.**
**Personalize the user’s experience by learning from their actions over time.**

**14 Update and adapt cautiously.**
**Limit disruptive changes when updating and adapting the AI system’s behaviors.**

**15 Encourage granular feedback.**
**Enable the user to provide feedback indicating their preferences during regular interaction with the AI system.**

**16 Convey the consequences of user actions.**
**Immediately update or convey how user actions will impact future behaviors of the AI system.**

**17 Provide global controls.**
**Allow the user to globally customize what the AI system monitors and how it behaves.**

**18 Notify users about changes.**
**Inform the user when the AI system adds or updates its capabilities.**
