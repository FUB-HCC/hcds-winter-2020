# Assignment 3
> **Date:** 14.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `ansa` Anil S.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the article inform your understanding of human centered data science?"  
Machines Learning is based on datasets. These datasets do not tell the 'full truth' about the problem that needs to be solved. As a developer we have to make sure that if we can reduce bias where it needs to be reduced that we do so. We cannot elimante bias but we can handle it properly.


### ❓&nbsp; Questions
_Using full sentences, list at least one question that this article raised in your mind, and say why it caused you to ask this question_

1. 

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [Repository](https://github.com/AnilSahintuerk/A3-hcds-hcc-bias)

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

  I found that some metrics which I would have considered as reasonable before the analysis in my opinion to support biases after. Especially countries with a tiny proportion of country population to region population were really misleading. Since they needed just a handful of articles just to be on the top coverage. And most of the countries which made it into the top coverage where also in the bottom relative quality table. I thought about it and could try to find an argument why this is like that. For some of them they are so unknown that they are published probably by locals but due to maybe some educational problems they cannot keep up with our standards of article quality. What also surprised me after the analysis that there are some countries with only one good quality article and they made it into the top ten relative quality. If I did not make any mistakes I would consider those resulst as not good and would not advise anyone to use them.

_Your 350 words_

1. _What is a good way to prepare for bias before starting the DS-Framwork? Predicting the tables and try to reason why I predicted it like that before the analysis. Would that be a good way?_

### Questions

Please answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    * population bias: Because countries with fewer population , fewer access internet and fewer education. Will have probalby not as many articles as other countries 
    * behavioral bias: harder to get good quality articles about countries with certain regimes (e.g. north korea)
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * _Data Filtering:_ Had to exclude some data because of typo differencies so merging the both csv files (given by alexa) e.g. Czechia and Czech Republic. And that also caused that for some countries the population was NaN so I could not consider them in the analysis.
1. What might your results suggest about (English) Wikipedia as a data source?
    * _The more a country is covered the more likely the quality is not good_
1. What might your results suggest about the internet and global society in general?
    * _There are not enough good articles especially in smaller countries with fewer access to internet and education. And that articles about politicians are written more in countries included in war e.g. Afghanistan_
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * _Yes if you create a model that tries to make a prediciton about relative article quality and education level_
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * _Yes when limiting the dataset to the "bigger" countries and comparing them to each other and not to their region. Then you may try to analyze why some countries do better than other countries_
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * _Seperate big and small countries and compare them to each other with out their region proportion (mitigate population and behavioral bias)
The region proportion distorts the results because a really small proportion just need 1 article to be in the top coverage which is obviously not true_
