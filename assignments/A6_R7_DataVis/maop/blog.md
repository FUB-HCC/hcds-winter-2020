# Assignment 6, Reading 7
> **Name:** `maop` Marc O.
> **Session:** [08 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/08_exercise)   
----

## R7 - Reflection
*Answer in at least 2-3 complete sentences the question "How does the reading inform your understanding of human-centered data science?".*

There are many barriers to human-AI interaction. A well-defined human design process can help to identify and solve these problems early on. In doing so, the problems that can arise in the development of human-AI systems should be less accepted as immutable. Rather, they should be investigated and justified in more detail so that sustainable solutions can be developed based on these challenges. The 18 guidelines can be used for this purpose.


*By reflecting on your sentences, list at least one question that occurred in your mind while reading, and explain your motivation for asking this question.*

The category of "when wrong" (G7-G11) seems particularly important to me. Therefore, I wonder if there is a prioritization in these guidelines, as I can imagine that not every one of these guidelines gets attention considering very short development times. A prioritization would help establish a ranking of importance in order to cover the most important aspects.

## `A6`- Guidelines for Human-AI interaction **[10 points]**
🕐&nbsp;&nbsp;&nbsp;**Deadline**: Mon, 2021-01-16 12:00 PM noon<br>
👥&nbsp;&nbsp;&nbsp;**Name**: Arne R.(`arro`), Malina S. (`masc`), Marc O. (`maop`)<br>

#### 1️⃣&nbsp;&nbsp;Preparation
1. ✅ Check out the section _Resources and concepts_ below, if you want to know more about the 18 Human-AI Guidelines, What-if-tool (WIT), COMPAS (dataset), or heuristic evaluations. This is **not mandatory**, but it should help you, if you need some more information or if you are just very curious!
1. ✅ Please note: The reading reflection (R7) will help you with this assignment. Please do this first. It lays the foundation regarding understanding the 18 human-AI interaction guidelines.
1. ✅ Please open the COMPAS Demo ➡️ https://pair-code.github.io/what-if-tool/demos/compas.html. We will evaluate this UI.
1. ✅ Please have the 18 guidelines open (examples for each are provided in the appendix of the original paper<sup>[2]</sup>).

#### 2️⃣&nbsp;&nbsp;Getting to know the context
1. ✅ What is the COMPAS dataset about? Describe the COMPAS dataset. **(3-4 sentences)**
* COMPAS is a landmark dataset to study algorithmic (un)fairness. This data was used to predict recidivism (whether a criminal will reoffend or not) in the USA. The tool was meant to overcome human biases and offer an algorithmic, fair solution to predict recidivism in a diverse population. However, the algorithm ended up propagating existing social biases and thus, offered an unfair algorithmic solution to the problem. In this dataset, a model to predict recidivism has already been fit and predicted probabilities and predicted status (yes/no) for recidivism have been concatenated to the original data.
2. ✅ What kind of unfairness did ProPublica found in their analysis? Check out the provided resources below. Especially check the article on ["Machine Bias"](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)<sup>[2]</sup> and focus on the following table. **(3-4 sentences)**
* ProPublica found that the tool inadvertently undermine the efforts made so far to ensure individualized and equal justice. The analysis exacerbates unwarranted and unjusts disparities that are already far too common in our criminal justice system and in our society. Also, the formula used in the algorithm formula was particularly likely to falsely flag black defendants as future criminals, wrongly labeling them this way at almost twice the rate as white defendants. In addition to that white defendants were mislabeled as low risk more often than black defendants. Speaking about racial discrimination, ProPublica found out that African Americans who didn’t re-offend, were labeled higher risk twice as often than whites. But ProPublica did not only find ethnic discriminations: A guy who has molested a small child every day for a year could still come out as a low risk because he probably has a job. Meanwhile, a drunk guy will look high risk because he’s homeless.

<center>
  
|                                           | WHITE | AFRICAN AMERICAN |
| ----------------------------------------- |-------|------------------|
| Labeled Higher Risk, But Didn’t Re-Offend | 23.5% | 44.9% |
| Labeled Lower Risk, Yet Did Re-Offend     | 47.7% | 28.0% |

</center>

#### 3️⃣&nbsp;&nbsp;Understand the ProPublica analysis (Task)
1. ✅ Please bring to your mind again, that **you** are evaluating the WIT. You can do no wrong!
1. ✅ Use the WIT (COMPAS Demo) to comprehend/understand the analysis result by ProPublica.
1. ✅ Please describe your thoughts (positive and negative), when first looking and exploring the tool. **(3-4 sentences in a pro/contra table)**

|       Pro       |                  Con                   |
|:---------------:|:--------------------------------------:|
|  powerful tool  | not intuitive                          |
| well documented | requires a lot of training to use      |
|                 | visual clutter at first glance         |
|                 | some input labels are cut off          |
|                 | few in app item descriptions available |

4. ✅ Note down (document) the steps you need to undertake in order to achieve a similar analysis result as ProPublica. **(steps, bullet points)**
   1. Working with the "What-If tool" we first tried to recreate the graphs from the article ["Machine Bias"](https://www.propublica.org/article/how-we-analyzed-the-compas-recidivism-algorithm) <sup>[2]</sup> in the datapoint editor tab. By setting **Binning | X-Axis** to `​Inference ​score`, **Count** to `10`, **Binning | Y-Axis** to `race` and **Color By** to `race`. All following fields were set to `default`. Quickly realizing that this tab is really just an datapoint view and there is no apparent way to plot the data in other form, the result was discarded. We tried around with the other features but got kinda stuck. In the end we used the provided steps from the sample solution.
5. If you get stuck (and please only if you get stuck!) ... follow the steps provided below → _Steps for analysis (backup)_

#### 4️⃣&nbsp;&nbsp;Documenting violations and flaws
1. ✅ Please read the 18 heuristics from the Human-AI Guidelines again.
1. ✅ Please bring to your mind again, that **you** are evaluating the WIT. You can do no wrong! 
1. Please inspect the UI again and look for violations (e.g. Are you missing anything in the interface? Is something misleading, unclear, or confusing?):
   * Describe the found issues briefly.
   * Assign the violated guideline.
   * Provide a screenshot with comments or annotations.
   * Please use the provided [template](https://docs.google.com/presentation/d/1762jwcZw9Hme5By7k3yV9oWPi_iT8UUB08_1Um9sRZM/edit?usp=sharing)(check out the [assignment folder](https://github.com/FUB-HCC/hcds-winter-2020/tree/main/assignments/A6_R7_DataVis) for `PPTX` and `ODP` files) to document your found issues.


Our presentation: [Here](https://docs.google.com/presentation/d/1slTr4yx4Mc3B3jB0nR7gIu_c67TpgJhfHLVF5T_XcDk/edit?usp=sharing)

#### Optional analysis
You can also use the "Exploration ideas" provided in the [colab notebook](https://colab.research.google.com/github/pair-code/what-if-tool/blob/master/WIT_COMPAS.ipynb) (scroll to the bottom!) to analyze the data even further.

### Deliverables
- [ ] PDF file with issues using the provided template
- [ ] blog.md files 

