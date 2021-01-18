# R7 Reflection - Data Visualization
> **Name:** `xiyu` Xin Y.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection
> Reading: _Guidelines for Human-AI Interaction_
1. How does the reading inform your understanding of human-centered data science?
<br> The AI system is most (semi-)autonomous and therefore it is different from traditional system with rigorous functions, requirements and design guidelines. Because of its (semi-) autonomy, the interaction between AI system and human beings are not easily to be predicted as well as formulized in a pre-design phase. This proposes different requirements for a human-AI interactive system. Microsoft therefore researched in different papers/research blogs etc. to synthesize different suggestions for a human-AI system design and formulated an at UI-level actionable design guideline for support for design decisions.
2. By reflecting on your sentences, list at least one question that occurred in your mind while reading, and explain your motivation for asking this question.
   <br> 1). I am curious about how a guideline for traditional HCI UI looks like, because the guideline seems to be too general. I can kinda understand that the research group may want to make it applicable for different AI-based system, but I don't know what considerations made specifically based on AI in formulation of this guideline. I would like to see how a Human-AI system guideline differs from a traditional one. 
   <br> 2). Combining G4 and G5, I currently don't know how a human-AI interaction system can show contextually relevant information and match social norms. For example social norms are heavily based on geograpical as well as social information, and sometimes they can be completely different (or even opposite). Does it mean that we should design completely different Human AI system for people from different social/cultural backgrounds? If not, how an AI system match the social norms. 
   <br> 3). For the part "when wrong": support "sufficient" ... seems a liitle bit vague for me. Is there any measurements or framework to see if a support is sufficient enough?


## A6 - Guidelines for Human-AI interaction
1️⃣  Preparation

1. Check out the section Resources and concepts below, if you want to know more about the 18 Human-AI Guidelines, What-if-tool (WIT), COMPAS (dataset), or heuristic evaluations. This is not mandatory, but it should help you, if you need some more information or if you are just very curious!
2. Please note: The reading reflection (R7) will help you with this assignment. Please do this first. It lays the foundation regarding understanding the 18 human-AI interaction guidelines.
3. Please open the COMPAS Demo ➡️ https://pair-code.github.io/what-if-tool/demos/compas.html. We will evaluate this UI.
4. Please have the 18 guidelines open (examples for each are provided in the appendix of the original paper[2]).

2️⃣  Getting to know the context
1. What is the COMPAS dataset about? Describe the COMPAS dataset. (3-4 sentences)
COMPAS is an algorithm used by judges and parole officers for scoring the likelihood of recidivism of a criminal defendant’s. The dataset contains personal information such as name, language, nationality, gender, age, status etc of over 10000 criminal defendets in Florida with their algorithm scores along with their outcomes within 2 years from 2013 to 2014. 
2. What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on "Machine Bias"[2] and focus on the following table. (3-4 sentences)

<center>
  
|                                           | WHITE | AFRICAN AMERICAN |
| ----------------------------------------- |-------|------------------|
| Labeled Higher Risk, But Didn’t Re-Offend | 23.5% | 44.9% |
| Labeled Lower Risk, Yet Did Re-Offend     | 47.7% | 28.0% |

</center>

There are generally two drawbacks:
(1) it doesn't work well on violent crime recidivism.
(2) biased in favor of white defendants but against black defendants.

Around 45% black defendents are considered as re-offending, whereas only 23.5% white defents are scored as high risky. The opporsite distribution shows the diaparity between the two groups. 

From the table we can see that, the black defendants were 
twice more probably to be wrongly labeled at high risk of re-offend. 

White defendants were often predicted to be less risky than they actually were. The white defendants who indeed re-offended were wrongly labeled twice as often as black re-offenders.

3️⃣  Understand the ProPublica analysis (Task)
1. Please bring to your mind again, that you are evaluating the WIT. You can do no wrong!
2. Use the WIT (COMPAS Demo) to comprehend/understand the analysis result by ProPublica.
3. Please describe your thoughts (positive and negative), when first looking and exploring the tool. (3-4 sentences in a pro/contra table)

<center>

| PRO                        | CONTRA              |
|:-------------------------  |:------------------ |
| demos with different tasks |not so easy to use  at first sight   |
| detailed readme file for first step   |  need a while for stepping in     |
||The visualization full of points was kind of confusing 
||L1/L2 counterfactuals unclear 


</center>

4. Note down (document) the steps you need to undertake in order to achieve a similar analysis result as ProPublica. (steps, bullet points)
5. If you get stuck (and please only if you get stuck!) ... follow the steps provided below → Steps for analysis (backup)
