## A5 - Explanations
<br>

> **Date:** 04.01.2021 - 14:47 PM *(Due: 11.01.2020 - 03:00 PM)*
> **Name:** `xiyu` Xin Y. and `goto` Gorgin T.
> **Session:** [07 Exercise - Explanations](https://github.com/FUB-HCC/hcds-winter-2020/wiki/07_exercise)   

----

### Task 1: Different Explanation Needs

#### ORES Scenario
Social science researchers may use the ORES model to discover and compare the online knowledge discourse sharing dynamics by assessing edit qualities of different topics on a specific wikimedia project. Take English Wikipedia for instance, the researchers may choose edits around different social debate topics such as "me too", "climate change", "covid 19" etc to discover how well is the knowledge base discussed on wikipedia. <br>
_Creators_: The Wikipedia group and the ML model designer. <br>
_Operator_: Researchers <br>
_Executors_: Researchers <br>
_Decision-Subjects_: Researchers <br>
_Data-Subjects_: selected articles on wikipedia <br>
_Examiners_: not sure if our scenarion contains examiners

To be a bit more specific, we will assume a more detailled scenario (wether or not it is realistic):
It's about a **magazine for birders**. They demand a system that assists them in finding changes regarding specific keywords: For example, the software should check from time to time if the article "starling" has changed. Imagine the ORES 'articlequality' score for that bird changed lately: This may indicate a higher interest for that bird by the public (just like "google trend") and therefore the editors might consider writing something about starlings in their next issue:

_Creators_: _Owners_ are the **programmers**: Agents who create and maintain said software that _uses_ ORES. The _Implementer_ of ORES itself are outside of this ecosystem.<br>
_Operator_: The software should be adjustable, e.g. the keywords should be changeable. it makes most sense if this is done by the same agents who are **executers**: <br>
_Executors_: these agents act on the results that the software gives to them, they're the part of the newspaper team who searches for topics to write aboout, we call them **topic hunters** as they dont necessarily have to be the writers themselves.<br>
_Decision-Subjects_: Agents affected by the decisions would be the **readers** (_also in a way the writers, their next task is subject to that decision, too_) <br>
_Data-Subjects_: **none** (there is no personal data used, just words) <br>
_Examiners_: **none**, since _examiners_ means "_agents auditing or investigating the ML system_" - here, that's the developers of ORES who are out of scope. However, if we were to extend our view, we could let the _creators_ examine the _significance_ of the (whole) systems outputs and, if necessary, adjust it (that includes using another ORES model).




#### Reflection

We think the role-based model should be considered throughout the human-centered design process. A data science project design using human-centered data science process should consider "human-in-the-loop"[1] element in the whole design process. As long as the users stand in the center of our design process, the concept of user-centric design has to be kept in mind. We then will specify why the users should be considered in different roles and examples are given on Image. 

**Analyse** : in analysis process, it is important to undertake requirements analysis to find out what features a system is supposed to have. It is about the expectations of the system from users. Since different roles have different expectations in the same use case, it is essential to use role-based model to find out what are expected from whom.

**Design for Usability**: In this stage, role-based model is important for interaction design. We may consider an explainable machine learning diagnostic system, doctors as operators as well as executors have different needs other than patients who are suffered from certain symptoms. 

**Evaluation**: Evaluation is important for testing the usage and usability. In machine learning system it is essential if the system will explain its results which "directly affect" users [GDPR, 2016]. Therefore, the user roles and evaluation of their perception of explanation should be considered in this stage.

**Feedback** : As mentioned in the first stage (analysis), different roles of users have different expectations on the system, in this case we should consider their feedback seperately and maybe have some tradeoffs for next iterative step. 



![Human Centered Design Process](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A5_Explanation/xiyu/Process%20of%20Human%20Centered%20Design.PNG)

---

### Task 2: Explanation method: LIME

[Link to the Github-repository](https://github.com/Nigrog/A7-hcds-hcc-explanations)

> LIME explanations for ID 22
<div>
<iframe src="https://github.com/Nigrog/A7-hcds-hcc-explanations/blob/main/exp_22.html"></iframe>
</div>

> LIME explanations for ID 42
<div>
<iframe src="https://github.com/Nigrog/A7-hcds-hcc-explanations/blob/main/exp_42.html"></iframe>
</div>
 
> LIME explanations for ID 60
<div>
<iframe src="https://github.com/Nigrog/A7-hcds-hcc-explanations/blob/main/exp_60.html"></iframe>
</div>

#### Reflection

1. Which documents did you choose?
    <br> We choose the documents 42, 60, 22. The documents are chosen completely randomly and arbitrarily.
2. What did you learn about the model?
    <br>The model gives local explanation by giving representitive feature sets. It also shows the users the weighted features, as how the marginal change in a feature will influence the classification result. 
3. How well do you think the classifier works? Why?
    <br> Generally Lime gives a good local explanation for classification, but the classifier seems not trustworthy by feature extraction. 
    * Advantages: The visualisation of representitive feature sets is clear and easy to understand. It represents the presence/absence of words. Additionaly, they designed a function for [fidelity and interpretability trade-off](https://design-ai.de/2020/04/01/lime.html) which garantees the accuracy of the model when producing understandable explanations for users.
    * Disadvantages: we only tested LIME with text data and it seems the LIME can only use single words as features but not word pairs or phrases. For example in our document classification, document 42 represents a result of Chrisitan and shows the word 'NOT' is highly seen as atheism. We doubt that whether the single word 'NOT' can be representitive. From our point of view, some feature words such as 'edu' are not that representitive for a classification in human logic.
4. For what role(s) (from task 1) are LIME explanations useful? Why?
<br> It can be useful for operators, executors and decision-subjects. In a scenario of credit issuing, operators nd executors can see why a credit applicant classified to qualified applicant or not. It the given representitive feature sets are meaningful and are in accordance with the decision attributes in human decision process, the result of classifier could be taken into consideration. Otherwise, the executors and the decision subjects can doubt the results. Additionally, it is good to see if some biased attributes (gender for example) are used in the classifier, decision subjects may refuse the result because of a biased case.
5. How useful is LIME for a non-data-scientist (e.g. non-ml-experts or designer)? Why?
<br> The answer to this question is similar to Q4. Decision subjects can clearly see why they are assigned to a class and for what reasons. They can see if they are biased and what influece different attributes have on their classification results.
6. What question types is LIME able to answer? Why?
<br> The explanation question types chould be: the reason of the classification, the marginal effect of respective attributes, etc. 

<div>
<iframe src="https://github.com/Nigrog/A7-hcds-hcc-explanations/blob/main/exp_22.html"></iframe>
</div>


#### References
1. Zanzotto, F. M. (2019). Human-in-the-loop Artificial Intelligence. Journal of Artificial Intelligence Research, 64, 243-252
1. Doshi-Velez, F., & Kim, B. (2017). Towards a rigorous science of interpretable machine learning. arXiv preprint arXiv:1702.08608.