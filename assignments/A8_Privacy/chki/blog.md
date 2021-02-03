# Privacy and Machine Learning
> **Name:** `chki` Christopher K .
> **Session:** [11 Exercise - Privacy](https://github.com/FUB-HCC/hcds-winter-2020/wiki/11_exercise)   
----

## Preparation

Franziska Boenisch is a researcher at Frauenhofer AISEC. Her area of research deals with privacy issues related to machine learning applications. These applications might allow reconstruction of parts of the training data as well as checking whether an individual is represented in the training data. She is currently researching in the area of Differential Privacy, a mathematical framework that provides formal privacy guarantees.

1. How can a system be protected that continously learns from user input? 
1. When thinking about security for ML systems, do we also need to consider the impact on HCDS principles? For example, in the beginning of the paper it was mentioned that ensembling different learners is a way improve security of ML systems by making the predictions private. This sounds like it could not only affect the system's performace but also negatively impact aspects like (intrinsic) interpretability.


## Summary


## Mind Map

I also include the link to Flinga since the image will be hard to decipher. I did not draw all too many connections between the lectures to keep the mind map as clean as possible.

![](chki_mind-map.png)
[Mindmap Flinga](https://flinga.fi/s/F9NMZU7)   

## Question
There was an example given in the lecture that showed the performance of a model that uses differential privacy with tuned hyperparameters. Even though it's performance was quite decent, many use cases require a better performance. Speaking from your experience, can you give some examples where a machine learning model using differential privacy performed really well?
## Takeways

* Machine Learning systems are very vulnerable (and often use sensitive data)
  * A lot more sensitive information can be gained as expected
* There are a couple of ways to tackle security and privacy issues but in general at the expense of model performance
* Differential Privacy uses the addition of noise to improve privacy of individuals that are represented in the learning data






