# Reflection 4 AI Fairness 360
> **Date:** 30.11.2020 - 21:18 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `xiyu` Xin Y.
> **Session:** [04 Exercise - Fairness](https://github.com/FUB-HCC/hcds-winter-2020/wiki/04_exercise)   
----

## R4 - Reflection
> Democast: Mitigating Discrimination and Bias with AI Fairness 360 - Democast #5

### 🗨️&nbsp; "How does the video inform your understanding of human-centered data science?"  

The video explains how to have a mindset of fairness concept into data work and how to apply the concept into data analysis pipeline. 
The workflow follows four general steps: Data-Check-Mitigate-Compare. First of all the data should be checked on its attributes, e.g. what is the favorable/unfavorable outcome and what labels are sensitive to bias which may lead to bias? In the check process, AI Fairness 360 used several different metrics for bias checking. In the mitigation phase, a variety of mitigation algorithms is provided to choose from based on research purpose. After processing, the mitigated result need to be compared with original outcome for validation. 
The [demo workflow](https://aif360.mybluemix.net/data) has a really clear struture in accordance with data analysis pipeline and we can clearly see that what additional steps or frameworks should be undertaken for each stage.
Additionally, I really liked the demo part of the step-by-step walkthrough in the Jupyter notebook to see how the Fairness Framework can be applied to bias mitigation for a certain use case/scenario with real code application.

### ❓&nbsp; Questions
1. Many fairness metrics are mentioned in this demo video. Is there any preference between them? I remembered when the speaker shows the demo, 4 out 5 metrics displayed bias, do the different metrics have different "Aussagekräfte", oder how should we understand when some metrics detect bias whereas others not?
1. For the data processing, unpriviledged attributes are ignored (in the Jupyter example), for some cases we can say that in advance that some attributes arise biases (such as gender/religion/personal status). But in some other cases, there could be some hidden attributes which can also cause bias, how should we detect them since they are hard to be discovered in advance?

***

## A3 - Wikipedia, ORES, and BIAS
Please, put everything regarding `A3` into the `blog.md` file of last week!