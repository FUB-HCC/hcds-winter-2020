# Reflection 7
> **Name:** `albe` Ali B.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection


**Answer in at least 2-3 complete sentences the question "How does the reading inform your understanding of human-centered data science?"**<br>

I think the main issue by designing interfaces for interacting with AI-infused systems is described very well with by the following sentence: *"AI components are inherently inconsistent due to poorly understood probabilistic behaviors on nuances of tasks and settings learned over time."*. The researches from Microsoft and the University of Washington developed and evaluated Design Guidelines to cope with the probabilistic and inconsistent behavior of AI. By reading the Design Guidelines the Dialogue principles from `ISO 9241-110` especially `controllability`, `error tolerance` and `conformity with user expectations` came to my mind. I think the introduced Guidelines are a good source to check for tackling difficulties from AI-infuced systems for fullfilling these principles. 



**By reflecting on your sentences, list at least one question that occurred in your mind while reading, and explain your motivation for asking this question.**

<br>

By reading the guidelines I noticed that the AI-infuced system should give feedback in many places. For example in G11 and G16. In G16 

it is mentioned that the system should give this feedback *Immediately*. I wonder if this immediate feedback may could interrupt the user 

experience? 


## A6 - Guidelines for Human-AI interaction


1. What is the COMPAS dataset about? Describe the COMPAS dataset.

The COMPAS Dataset is a dataset about criminal offenders screened in Florida (US) during 2013-14 and contains data about 5855 observations. It contains features with numeric values like `number of juvenile felonies`, `number of juvenile misdemeanors`, `age` etc. and categorical feature values like `sex` and `race`. The ground truth feature `recidivism_within_2_years` is if the offender was recidivism within the timeframe of 2 years. It was a bit difficult to find description of the features but finally I could find this one 
[here](https://rdrr.io/cran/fairml/man/compas.html).

5 categorical values like Inference value, Inference
