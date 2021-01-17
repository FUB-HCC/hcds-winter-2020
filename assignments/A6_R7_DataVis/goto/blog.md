# Guidelines for Human-AI Interaction
> **Name:** `goto` Gorgin T.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## `R7` - Reflection
Please read (at least!) page three of the paper [Guidelines for Human-AI Interaction](https://www.microsoft.com/en-us/research/uploads/prod/2019/01/Guidelines-for-Human-AI-Interaction-camera-ready.pdf) <sup>[1]</sup>.

> 1. Answer in at least 2-3 complete sentences the question _"How does the reading inform your understanding of human-centered data science?"_. </br>
> 2. By reflecting on your sentences, list at least one question that occurred in your mind while reading, and explain your motivation for asking this question.

##### **Topic:** The core of the paper is a set of _18 guidelines for Human-AI Interaction_ [which] _are grouped into four sections that prescribe how an AI system should behave upon initial interaction, as the user interacts with the system, when the system is wrong, and over time._<sup>[2]</sup>

The "humble" introduction from the blog<sup>[2]</sup>, stating that each guideline should be seen as a suggestion and the level of implementation can vary and change, reminded me  of the importance of _perception_: If I was to implement an AI into a system (actually, when creating any software), then I must not forget that my perception can be different to others. In conclusion, the guideline confirmed for me that for building better software, an important factor is scientific research on human perception (and _not_ my personal understanding of usability).

So, the 18 G's might come in handy, they all make sense and should be considered.


_Question/thought:_</br>
Not really about my own sentences: At first, I got G13 (_Learn from user behavior_) wrong. It says, that a core element of the software is supposed to use AI to incorporate user's decisions, like a route planner learns from what routes the user selects.
I thought it suggests to "extend the AI-system with more AI": The navigation system could also learn when I tend to miss directions (lame example: After work I am tired) and hence tell me instructions earlier, speak louder and slower etc., or tell my radio to play slower songs on Monday morning because I tend to speed then, etc.</br>
Could it be useful to reach into domains usually not part of the system?

Maybe that's silly but I found it interesting :) 
</br></br>

---
---
---
</br>

## `A6`- Guidelines for Human-AI interaction **[10 points]**

🕐&nbsp;&nbsp;&nbsp;**Deadline**: Mon, 2021-01-16 12:00 PM noon (ONE week)<br>
👥&nbsp;&nbsp;&nbsp;**Delivery mode**: groups of two students (same groups as last time)<br>

🥅&nbsp;&nbsp;&nbsp;**Goals**
1. Getting familiar with the design guidelines for human-AI interaction.
2. Evaluate the user interface of the What-if-tool.
3. Understand the ProPublica analysis on "Machine Bias".

The goal of this assignment is to **evaluate the usability of the _What-if-tool_'s user interface**, by finding violations and flaws (in the UI) against the guidelines/heuristics. In this assignment you will use an (informal) usability inspection method from the field of HCI called heuristic evaluation. It is not necessary for you to know this method in detail, because you will be guided through this (slightly adapted) process (Steps 1️⃣&nbsp;&nbsp; to 4️⃣&nbsp;) The **main task** is to find violations and flaws in the given UI and assign each issues to one of the 18 guidelines (heuristics).

### Instructions
#### 1️⃣&nbsp;&nbsp;Preparation

1. Check out the section _Resources and concepts_ below, if you want to know more about the 18 Human-AI Guidelines, What-if-tool (WIT), COMPAS (dataset), or heuristic evaluations. This is **not mandatory**, but it should help you, if you need some more information or if you are just very curious!
1. Please note: The reading reflection (R7) will help you with this assignment. Please do this first. It lays the foundation regarding understanding the 18 human-AI interaction guidelines.
1. Please open the COMPAS Demo ➡️ https://pair-code.github.io/what-if-tool/demos/compas.html. We will evaluate this UI.
1. Please have the 18 guidelines open (examples for each are provided in the appendix of the original paper<sup>[2]</sup>).


#### 2️⃣&nbsp;&nbsp;Getting to know the context
1. What is the COMPAS dataset about? Describe the COMPAS dataset. **(3-4 sentences)**

> **C**orrectional **O**ffender **M**anagement **P**rofiling for **A**lternative **S**anctions is "_is a case management and decision support tool_ [...] _used by U.S. courts to assess the likelihood of a defendant becoming a recidivist._ <sup>[a]</sup>"
> About the actual dataset, we cite the [Practitioner's Gude to COMPAS Core](https://assets.documentcloud.org/documents/2840784/Practitioner-s-Guide-to-COMPAS-Core.pdf), Chapter 2.9 Norm Groups (page 11):
> ###### **The COMPAS Core normative data were sampled from over 30,000 COMPAS Core assessments conducted between January 2004 and November 2005 at prison, parole, jail and probation sites across the United States.** The Core Norm Group was compiled to obtain proportions of prison, parole, jail, and probation assessment data that reflect proportions of adult correctional populations in the criminal justice system. Based on recent criminal justice statistics, 21.6% of persons under adult correctional supervision during 2011 were in prison, 12.2% were on parole, 10.5% were in jail, and 56.9% were on probation (Bureau of Justice Statistics, 2012). The Composite Norm Group consists of assessments from state prisons and parole agencies (33.8%); jails (13.6%); and probation agencies (52.6%). The Core Norm includes 7,381 offenders. Men represent 76.9% of the Core Norm Group (n=5,681), and women represent 23.1% of the Core Norm Group (n=1,700). The median age at assessment is 31.0 (M = 32.6) in the Core Norm Group. **The racial composition of the Core Norm Group is 61.6% Caucasian, 24.9% Black, 10.3% Latino and 3.2% other racial groups.**
> 


</br>
1. What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on ["Machine Bias"](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)<sup>[2]</sup> and focus on the following table. **(3-4 sentences)**

|                                           | WHITE | AFRICAN AMERICAN |
| ----------------------------------------- |-------|------------------|
| Labeled Higher Risk, But Didn’t Re-Offend | 23.5% | 44.9% |
| Labeled Lower Risk, Yet Did Re-Offend     | 47.7% | 28.0% |

</br>

> The unfairness they found was racial bias: The percentages for labelling the risk is highly different for black people as it is for white people: Of the blacks labelled as "Higher risk", half of them re-offended, half did not. For whites though, about 3/4 of them _did_ re-offend.
> Also: For people marked as "Lower Risk", about 1/4 of the blacks re-offended. Double as much whites re-offended. </br>
>  Interestingly though, this happened without a _direct_ connection to race: "_We ran a statistical test that isolated the effect of race from criminal history and recidivism, as well as from defendants’ age and gender._" and _"Northpointe’s core product is a set of scores derived from 137 questions that are either answered by defendants or pulled from criminal records. Race is not one of the questions."_ <sup>[2]</sup> Apparently the date does indeed "_include items that can be correlated with race — such as poverty, joblessness and social marginalization._"


#### 3️⃣&nbsp;&nbsp;Understand the ProPublica analysis (Task)
1. Please bring to your mind again, that **you** are evaluating the WIT. You can do no wrong!
1. Use the WIT (COMPAS Demo) to comprehend/understand the analysis result by ProPublica.
1. Please describe your thoughts (positive and negative), when first looking and exploring the tool. **(3-4 sentences in a pro/contra table)**
1. Note down (document) the steps you need to undertake in order to achieve a similar analysis result as ProPublica. **(steps, bullet points)**
1. If you get stuck (and please only if you get stuck!) ... follow the steps provided below → _Steps for analysis (backup)_

#### 4️⃣&nbsp;&nbsp;Documenting violations and flaws
1. Please read the 18 heuristics from the Human-AI Guidelines again.
1. Please bring to your mind again, that **you** are evaluating the WIT. You can do no wrong! 
1. Please inspect the UI again and look for violations (e.g. Are you missing anything in the interface? Is something misleading, unclear, or confusing?):
   * Describe the found issues briefly.
   * Assign the violated guideline.
   * Provide a screenshot with comments or annotations.
   * Please use the provided [template](https://docs.google.com/presentation/d/1762jwcZw9Hme5By7k3yV9oWPi_iT8UUB08_1Um9sRZM/edit?usp=sharing)(check out the [assignment folder](https://github.com/FUB-HCC/hcds-winter-2020/tree/main/assignments/A6_R7_DataVis) for `PPTX` and `ODP` files) to document your found issues.

#### Optional analysis
You can also use the "Exploration ideas" provided in the [colab notebook](https://colab.research.google.com/github/pair-code/what-if-tool/blob/master/WIT_COMPAS.ipynb) (scroll to the bottom!) to analyze the data even further.

### Deliverables
- [ ] PDF file with issues using the provided template
- [ ] blog.md files

### Steps for analysis (backup❗)
💡 Please only read if you are _very_ stuck.<br>
Source: https://colab.research.google.com/github/pair-code/what-if-tool/blob/master/WIT_COMPAS.ipynb#scrollTo=bOVamCz1LsTd

> We can see the same unfairness that ProPublica found in their analysis by:
> 1. Going the the "Performance + Fairness" tab
> 1. Setting "Ground Truth Feature" to "recidivism_within_2_years"
> 1. In "Slice by" dropdown menu, select "race"
> 1. Look at the confusion matrices of the "African-American" and "Causasian" slices.
>    * They have very similar accuracy (TP+TN)/Total
>    * But, the FP rate is MUCH higher for African Americans and the FN rate is MUCH higher for caucasians

## Session Blogs
1. `alsc` [My title - This is a template, please use!](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A6_R7_DataVis/alsc/blog.md)
1. `maop` [Assignment 6](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A6_R7_DataVis/maop/blog.md)
1. `ansa` [Assignment 6](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A6_R7_DataVis/ansa/blog.md)


***
### References, Resources and concepts

_Human-AI Guidelines (Heuristics)_
* Microsoft Research blog post ["Guidelines for human-AI interaction design"](https://www.microsoft.com/en-us/research/blog/guidelines-for-human-ai-interaction-design/)
* Original CHI'19 Paper: see references at the bottom

_What if tool (WIT) and COMPAS demo_
* [Website](https://pair-code.github.io/what-if-tool/) and [GitHub](https://github.com/pair-code/what-if-tool) of the What-if-tool
* [What-If Tool demo](https://pair-code.github.io/what-if-tool/demos/compas.html) - binary classifier for predicting recidivism - COMPAS dataset
* WIT COMPAS [colab notebook](https://colab.research.google.com/github/pair-code/what-if-tool/blob/master/WIT_COMPAS.ipynb)

_More infos on COMPAS_
* https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing
* https://www.propublica.org/article/how-we-analyzed-the-compas-recidivism-algorithm
* http://www.crj.org/assets/2017/07/9_Machine_bias_rejoinder.pdf
* https://pair-code.github.io/what-if-tool/demos/compas.html
* Dataset on kaggle: https://www.kaggle.com/danofer/compass

_Heuristic Evaluation_
* https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/
* https://www.interaction-design.org/literature/topics/heuristic-evaluation#:~:text=Heuristic%20evaluation%20is%20a%20process,usability%20from%20early%20in%20development.

<sup>[1]</sup> S. Amershi et al., “Guidelines for Human-AI Interaction,” in Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems, Glasgow, Scotland Uk, May 2019, pp. 1–13, doi: 10.1145/3290605.3300233.<br>
<sup>[2]</sup> Angwin, Julia, et al. "Machine bias. ProPublica." See https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing (2016).

[1] S. Amershi et al., “Guidelines for Human-AI Interaction,” in Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems, Glasgow, Scotland Uk, May 2019, pp. 1–13, doi: 10.1145/3290605.3300233.

[2] [Microsoft Research Blog](https://www.microsoft.com/en-us/research/blog/guidelines-for-human-ai-interaction-design/)


[a] https://en.wikipedia.org/wiki/COMPAS_(software)