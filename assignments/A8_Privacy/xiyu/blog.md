# 11 Session - Privacy and Security
> **Name:** `xiyu` Xin Y.
> **Session:** [11 Session - Privacy and Security](https://github.com/FUB-HCC/hcds-winter-2020/wiki/10_exercise)   
----

## Preparation

_Franziska Boenisch completed her Bachelor and Master's degrees in Computer Science from Free University of Berlin and has plenty of academic research experience in machine learning as well as data privacy. She is now a research associate of Fraunhofer with focus on privacy preserving Machine Learning and data protection._ 

1. In the paper (page 2) is mentioned that "ensembling different learning systems is one of the ways to improve ML security (e.g., having an ensemble of learners vote for a prediction can make this prediction private". I don't really understand the sentence by:<br>
    1.1 Why using emsemble learning systems will improve security? By making the system more intransparent and complicated?
    1.2 How can we combine different learning systems? Will the ensembling decrease the system's performance?
1. In the section 4, it seems that there are generally two approaches for model assurance: data protection (pre-model) and system auditing (post-model). I was wondering if there is many systems which continously learn and train, which means there is no clearly separating phases of training and testing. Therefore, the methods mentioned in Section 4.1 and 4.2 seem cannot protect system from attacks at runtime well. Is there any protecting system which recognizes unwilling attacks or manipulation at runtime?


## Summary
_approximately 250 words_

The guest lecture is about privacy preserving in machine learning systems. The presentation is structured into 4 parts: Background, Privacy Risks and Attacks again ML system; Privacy Preserving Techniques and Differential Privacy.

Franziska first introduces the concepts of privacy attacks and machine learning. She introduces the concepts based on an example of netflix to help to understand how attacks can appear in our daily life. She then introduces where are attacks easily appearing in ML systems and how adversaries will attack a ML system and therefore to achieve their adversarial goals.

In the second part, Franziska talks about privacy attacks against ML system. She stressed that, even though ML system always considered as a blackbox and lacks transparency, the process still doesn't correspond to anonymization and is (partially) reversable. She introduced four different attacks: model inversion, attribute inference, membership inference and model extraction. She used different examples for each kind of attacks to show audience how the model details can be (partially) uncovered by adversarials.

Franziska then talked about several privacy preserving techniques in order to prevent from information leakage and to ensure data privacy. She talked about 4 different techniques - including homomorphic encryption, federated learning, secure multiparty computation and differential privacy - and mentioned that some ML setting parameters are important for an adequate choice of privacy presering technique. After introducing the general ideas of the first three techniques, she explained differential privacy more in details based on her personal research focus.

The idea of differential privacy is to incorporate random noise into the data statsitics which can make the ML system resilient to adaptive attacks that use auxiliary information. The differential privacy algorithms will make the data statistics more noisy as well as imprecise but it shouldn't distort the analysis of original data set, which means the data set with noise should roughly have the same result as the original one. Adding noise into the data is an essential point of this algorithm, and it is important to consider where to add noise into the system: training data, prediction output or training process. Franziska explained the differential privacy stochastic gradient descent and compared the DP-SGD algorithm with the SGD algorithm without privacy to show how the noise works in a model and how it can help to preserve the privacy. 

At last but not least, she emphasizes that privacy preserving depends on correct conceptualization and correct use of different techniques, an efficient privacy preserving system depends on coporative disciplinary work-together. 






## Mind Map

* My Mind Map 
![Concept Map of Human Centered Data Science](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A8_Privacy/xiyu/xiyu_mind-map.png)


## Question
1. Are transparent models more easily to be attacked? 
1. Is there any reverse relationship between openness/explainability/... to privacy and security? On the slide it is said even though many ML systems are considered as blackbox, the process still doesn't correspond to anonymization and is (partially) reversable. Does it mean that if we use some transparent tool (like IBM 360) or explainability tool, it will not only make users understand it, but will also help adversarials understand the inner processes of the model and therefore help them to unbox the ML system?
1. For differential privacy, I don't really understand the part of adding noise based on Gaussian or Laplace distribution. What's the differece of both noise and how will they differently influence the performance of DP-SGD algorithm?


## Takeways

I think it is important for me to keep the threat space and the previous questions of privacy preserving techniques in mind before designing a ML system. For example, I should know in design process where could privacy threats appear and what kind of attacks am I or are users possibly going to face? When choosing techniques for my ML system, I should first define how many parties will be included in the training process, where should the training and prediction take place etc. I have to be really carefule and be aware of those potential threats when design a ML system at an early stage.  
