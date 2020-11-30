# Assignment 3 - Bias
> **Date:** 14.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `albe` Ali Bektas
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  
_In at least 2-3 full sentences, answer the question "How does the video inform your understanding of human centered data science?"._

The main takeaway from this paper for me was that technical artefacts such as the model and the data for the model is not just a passive technical tool but gains agency through everyday use. From the reading of this paper I understand that these systems strengthening biases which are present in the real world as they produce categories produce categories using statistical methods on the data and imply meaning in 
a specific context. 
My understanding of human centered data science is to work on methods coping with these kind of biases in the favor of the humans 
and the society while creating data science solutions.


### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. In the case of the AMS Algorithm the question arises in me if it is not more of a conceptual error in matter of how and for which 

purpose the system is used for then the output it generates? In our current society it is not a secret that some groups of people

are disadvantaged based on some attributes they have (or they get assigned). Isn't it good that the algorithm mirrors the reality? 

Could this information not be used to have a good impact on the society. For example the AMS reasons investigate the circumstances why 

these group of people has a lesser chance to get integrated to the job market and create initiatives to help them. 



There are groups of people where it is more obvious that they are disadvantaged int many situations (eg. Womans, Homosexuals, People with foreign sounding names). But there are maybe also groups where it is not so obvious that they for what reason ever disadvantaged. 

Because such as they live in the wrong street, their parents had not the a higher education and maybe some more which are not know.

If the system is designed to find such attributes to support these people I think it is a good thing that the algorithm points 

out such biases. The question then is still if this bias really in the reality or only in the data the algorithm is trains with. 

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** https://github.com/Alioio/A3-hcds-hcc-bias

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

I learned that the data which is used for the analysis should be questioned in terms of different kind of biases and should be checked 
if it is usefull to answer the reaserch question before starting the analysis. In the case of the data used in this assignment one main 
source of bias was the population dataset for various reasons. There were countries where the population was very unbalanced. 
Analysis was done based on relative amount of population and countries with very less populations were compared with countries with high population. Second there was an error in the dataset. The countries were represented in two different units. Some countries were represented in millions and some in tausends which made results where this dataset was used unreliable. Another issue when comparing countries differing in geographical location and differnt population I could imagine is that some of these countries are not as much known in the sociey and 
especialy in the group of wikipedia authors. This could be the reason for some countries having eigher less amount of articles and/ or lower 
quality articles. 

Another source of bias I could imagine is the used ORES API for this assignment. Documentaion for the API is available but to be honest. In this short time it was not possible for me to fully understand how the API and the underlying machine learning model is working and how it had been trained. 

1. Is there a systematic method or framework available how such kind of biases can be detected before starting analysis?

### Questions

Please answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    * I expected to find biases for countries which are not so well known in the group of wikipedia authors and in the society as whole. 
    
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
        * By filtering data and excluding countries durring merging of the two datasets wikipedia data and the population data which was provided in the assignment. Some of this countries were excluded because of diffrent writing. 
    
1. What might your results suggest about (English) Wikipedia as a data source?
        * The less a country is known by the group of wikipedia authors and the society the less articles about their politicians are available with higher quality. 
    
1. What might your results suggest about the internet and global society in general?
    * Access to internet, a good education system and is playing an important role to have a higher number of good quality articles. 
    I think of countries where the access to information is limited because of lack in good education system, infrastructure or authoritive 
    gouvernment. 
    
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * I think one could gather insights about the ralation of article quality and the level of education, access to internet or the effects of differnt regimes do have to article quality. 
    
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * Yes by not comparing all countries but countries which are similar in regards to population and geographical location. 
    
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * Yes. Maybe by not comparing all countries but grouping them into clusters and comparing countries inside the same cluster. For example countries with lower polulation and countries with higher population. 
    Second (but this requires to include other data sources): By not only taking the population size as an indicator and including other indicators as well such as an indicator for access to internet, education level, political situation and so on. 
