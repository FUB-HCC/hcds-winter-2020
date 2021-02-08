# Assignment 8 - Privacy and Security
> **Name:** `jowe` Jonas W.
> **Session:** [11 Exercise - Privacy and Security](https://github.com/FUB-HCC/hcds-winter-2020/wiki/11_exercise)   
----

## 1 - Summary

The guest lecture was about privacy and security risks when working with machine learning systems. At first the basics of privacy as well as machine learning systems and how they are trained were explained. Afterwards multiple scenarios were discussed, varying by the way the attackers have access to the model, for example. Such as having full knowledge of the inner workings and access to the code, only being able to access the system through limited API calls, being able to influence the training of the model or not, and so on. Other notable scenarios were the creation of a copy model, behaving like the targeted model without having access to it, which seemed especially important in industry scenarios. Also the possibility of identifying specific individuals even when having very limited pseudonymized data was discussed. For each of these scenarios specific possible solutions were explained, including dispersing the model training to multiple end devices or cryptographic solutions. A reoccuring theme in these solutions was also the addition of noise to the data. In the end it was concluded that privacy is a very important topic when working with machine learning systems and data, which needs to be handled to protect the individuals behind the data as well as the model itself. The possible solutions need to be understood and implemented thoroughly even if it leads to an increase in work and a performance overhead.

## 2 - Mindmap
![](jowe_mind-map.png)

## 3 - Question
- Do you believe that data protection laws such as GDPR need to further include and stricten parts about machine learning systems and the data protection when working with them to ensure the people producing them are doing their best to handle the possible risks when working with often sensitive and identifying data?

## 4
While the different solutions explained were interesting, I think the part which was the most useful immediately was the general idea that privacy and security issues need to be kept in mind at all times when working with machine learning systems, even when the model/data seems to be safe e. g. when only accesible through limited API calls or when using pseudonymized data like in the Netflix example. While this idea is obviously not new, having information about the different scenarios and attack vectors and some specific ideas on how to handle them, helps to think about this point when creating systems like this.
