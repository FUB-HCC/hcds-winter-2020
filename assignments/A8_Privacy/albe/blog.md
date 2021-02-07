# Assignment 8 - Privacy and Security
> **Name:** `albe` Ali B.
> **Session:** [11 Exercise - Privacy and Security](https://github.com/FUB-HCC/hcds-winter-2020/wiki/11_exercise)   
----

## Preparation

Fanziska Boehnisch is a research associate at Fraunhofer AISEC (Applied and Integrated Security) and makes currently her PhD at the Freie Universität Berlin and is theaching there in security and privicy related topics. Her research field is locted at the intersection of Machine Learning and Data Privacy. [[1]](https://franziska-boenisch.de/) [[2]](https://www.mi.fu-berlin.de/inf/groups/ag-idm/members/4_Mitarbeiter_innen_SSE/Franziska-Boenisch/index.html)

1. Are there different levels of data privacy and security requirements for different sort of project? If so are there design guidelines or so a checklist available what can be used in the design or evaluation phase of a software development process? 

2. When designing an AI-infused system or application are there and viewing different aspects like accuracy, computational cost, user experience does it sometimes appear that 
these aspects are conflicting with the privacy and security aspect? Is a tradeoff in some situations is required?

 ## Summary
The guest lecture gave an introduction to vulnerability of ML Systems, privacy and security issues and gave and overview on how to threat these issues. 
Boenish first gave a brief introduction about privacy, information leakage and privacy leakage. She then explained main concepts on how machine learning 
models work and how they trained. 

She then gave an overview about possible sources of threats against the ML System. She explained these possible threats in different scenarios 
involving different attackers with varying knowledge, capabilities and goals. 

After this introduction into the topic she presented different examples of attack followed by possible solutions for these attacks. 
`Model inversion` is a type of attack where and attacker tries to use the model to model the training data or a representation of the training classes. 
In the case of an `attribute inference attack` the attacker tries to infer secret attributes of an model. If the attackers goal is to find out if a 
concrete data point was used to train the model he would make an attack called `membership inference attack`. In an scenario where the attacker tries 
to understand and imitate the model's functionality or tries one speak about an `model extraction attack`.



After presenting the different types of attacks Boehnisch explained different techniques how these attacks can be defended or prevented. 

With the help of `Homomorphic Encription` for example it is possible to keep the model private (e.g. on the mobile device) while training it on a cloud. In the 
last part of the lecture she explained methods which are called `differenctial privacy`. In these methods the some noise is added to the data and\or the weights 
of the model to make the inference of private information harder for attackers. She concluded these methods with some examples she showed us which showed the 
that the the accuracy of the model could be slightly decreased with applying this methods and it could be difficult the find the right parameters. So there is 
some tradeoff between better performance and better privacy in the end. 

## Mind Map


## Question
...?

## Takeways
...
