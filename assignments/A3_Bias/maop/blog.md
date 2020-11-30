# Assignment 3
> **Date:** 14.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `maop` Marc O.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  
_In at least 2-3 full sentences, answer the question "How does the video inform your understanding of human centered data science?"._
Research ethics plays a fundamental role, especially when publishing an algorithm in legal areas. The system must be transparent and decisions must be easily verifiable. This algorithm has been a perfect example of how discrimination against women in the labor market is beeing increased if ethical aspects and  are not considered properly. Even if such an algorithm only serves as a decision-making aid for human counsellors, it must be ensured that the computer's judgements would become irrevocable in practice in order not to further cement discrimination.

### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. Is there a way to scientifically prove the impartiality of such an algorithm? Can we demolish the boundary between empirical observations and questionable decisions and categorizations of the system?
1. More transparency inevitably means a longer development time. When is a system transparent enough to be free of prejudices and bias? 
1. How to take the pressure off the development team in order to enable the selection of suitable data as the basis of bigger data science projects?

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** `<add link to our repo here>`

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.


_I came across the realization that it is important to check his data again. For example, many countries have been skipped out because they were named differently in the `export_2019.csv` than in the `page_data.csv`. This could have been avoided by manually checking the country names and adjusting them if necessary. Similarly, the population in the `export_2019.csv` was not necessarily correct, so that these data records may lead to an incorrect result. In addition, I wondered whether this representation might not encourage certain prejudices: Countries that have few articles about politicians in the English-language Wikipedia are thus rated lower. It is quite possible that these countries have excellent articles in their national language, but the absence of the English article will lower their ranking.
Furthermore, it is questionable which aspects are included in the "ORES" score prediction and whether they favour politicians who are not well-known in the English-speaking world. It is obvious that famous politicians in the English-speaking world usually enjoy a higher degree of popularity than "smaller, less well-known" politicians. This leads to the fact that famous politicians have a more popular article, which in turn is more likely to be edited, since there are simply more sources and information available for it.
In fact I was surprised about the significance of a rev_id, which indicates the frequency of editing an article, from which one can then predict the quality of an article. It was also interesting to see how long a data query via the "ORES API" takes. This could indicate a high complexity of the underlying algorithm. However, it was more important to develop an efficient query method.
In this assignment I learned the importance of a reproducible project and learned to appreciate its importance. Since I worked on this project on several days, it was important to export data sets as csv so that they could be reused at a later time. It was at least as important to think about the extent to which these data could have been manipulated. This brings me back to my initial doubts about the credibility of the data sets resulting from the project_


1. _How about taking more the the English Wikipedia into consideration? Does this lead to a satisfying result?_
1. _How can one be sure, that either the revisions or the ORES prediction are trustworthy enough and retrievable at a later date?_

### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    * _I expected to find biases againt countries that do not use english as their official language. This doubt is due to the fact that in an English-speaking country there are more English language articles_
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * _I discovered a wrong scaling of certain values. E.g. Population data has not always been given in millions, so this might falsifies the result._
1. What might your results suggest about (English) Wikipedia as a data source?
    * _English Wikipedia indirectly favors English speaking countries. From an English speaking country there are logically "better" articles than from countries, which have another official language than English_
1. What might your results suggest about the internet and global society in general?
    * _English speaking countries get definitely more attention. This puts all other countries in the background. It would also be interesting to know if you could not only get the English Wikipedia as a source._
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * _An example could be, if you want to expand with a company and use such a project as a basis for market research, you should have processed enough prejudices directly and indirectly, so that the output data does not necessarily reflect reality_
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * _A possible research situation could be the attempt to measure the willingness of a population group in a country to work on such articles. Furthermore, it could be used to determine if the article quality rate is increasing depending on the number of involved users._
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * First of all, the population data must be corrected. Furthermore, not only specific country names should be queried, but also their variations or ankronyms (Czechia (`export_2019.csv`) vs. Czech Republic (`page_data.csv`)). This cound be a possible solution.
