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


1. **What is the COMPAS dataset about? Describe the COMPAS dataset.**

The COMPAS Dataset is a dataset about criminal offenders screened in Florida (US) during 2013-14 and contains data about 5855 observations. It contains features with numeric values like `number of juvenile felonies`, `number of juvenile misdemeanors`, `age` etc. and categorical feature values like `sex` and `race`. The ground truth feature `recidivism_within_2_years` is if the offender was recidivism within the timeframe of 2 years. It was a bit difficult to find description of the features but finally I could find this one 

[here](https://rdrr.io/cran/fairml/man/compas.html).

1. **What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on "Machine Bias"[2] and focus on the following table.**

By considering the analysis results that Black defendants have more risk to being labeled as "High risk" when they actually does not re-offend [see Table under 'Prediction Fails Differently for Black Defendants](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing) for me it looks like that the model violates the fairness definition `Predictive Parity`. 

>*"A classifier satisfies this definition if both protected and unprotected groups have equal PPV – the probability of a subject with positive predictive value to truly belong to the positive class."* 

In the case of COMPAS: **P(Y = "Low Risk" | d = "Low Risk", G = "Caucasian") = P(Y = "Low Risk" | d = "Low Risk", G = "African-American")**

When viewing the distribution plot shown in the [https://www.propublica.org/article/how-we-analyzed-the-compas-recidivism-algorithm](Analysis) section of prorepublica, we see that the distribution of risk scores for black defendants is different then for white defendants to the disadvantage of black defendants. Viewing the the restuls with considering the probability scores it also looks like the model is also violating fairness definition `Test Fairness`.

> *A classifier satisfies this definition if for any predicted probability score S, subjects in both protected and unprotected groups have equal probability to truly belong to the positive class.*<br>

In the case of COMPAS: **P(Y = "Low Risk" |S = s, G =  "Caucasian") = P(Y = "Low Risk" |S = s, G = "African-American" )**

