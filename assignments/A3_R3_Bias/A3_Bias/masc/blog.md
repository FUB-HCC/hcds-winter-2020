# Assignment 3
> **Date:** 14.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `masc` Malina S.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  
I found the article very interesting as it shows how important it is to think about the ethical consequences when implementing a technical system, especially if it is being designed for the public sector. It further illustrates that the quality of an algorithm does not just depend on its technical efficiency but also on its practical implication. The algorithm might classify cases very accurately and correctly but still not be designed for society's needs. 

### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. Who developed the algorithm? Did the consist in comupter scientists only or was there people with other backgrounds involved?
1. I wondered why the algorithm did not include the job seekers needs but only their demographics? Wouldn't the classification  be more useful if it integrated the job seeker's personal struggles such as discrimination (if they belong to a minority group), health issues (in case of chronic illnesses)... ?

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [A3-hcds-hcc-bias](https://github.com/malina-scheuer/A3-hcds-hcc-bias)

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

Conducting this project was very interesting to me as I had never worked with ORES before and did not even know that a scoring system for assessing the quality of wikipedia articles exists. I am pleased to know that such a database exists and I think it is important to use it in relation with analyzing wikipedia data. Since wikipedia is an open-source platform and articles can be written and edited by anyone. Therefore, high quality content is not always guaranteed. However, wikipedia is a powerful platform which has an influence on public knowledge and opinion. Analyzing its content can therefore lead to interesting inisghts, especially in the context of looking at wikipedia articles with political content. The quality and amount of political wikipedia articles can be a reflection of the political system of a country.

I was very suprised when I saw the results of my analysis. I expected more Western countries in the Top 10 in terms of coverage and relative quality. Furthermore, I found it interesting to see that there is no relation between high coverage and high quality. None of the top 10 countries with high coverage also appeared in the top 10 of countries with high quality. It therefore seems like the amount of high quality articles is not the same in all countries and it does not increase linear with the amount of articles beeing written. This also means that in countries with high coverage there might be a high amount of bad quality articles which could lead to misinformation of the public. Another fact which really suprised me was the amount of non-democratic countries in the top 10 for relative quality. I was wondering whether internet restrictions and sanctions might limit the amount of bad quality wikipedia articles.

To further investigate this issue and to find out whether there is a correlation between quality and coverage, statistical analysis would need to be performed. However, the analysis of this project already shed light on an important issue and raised interesting questions. It furthermore showed me the importance of putting numbers into perspective and rather looking at relative scores than absolute numbers.

1. Why are there so many non-democratic countries in the top 10 of countries with high amount of high quality articles?
1. Is there a significant correlation between coverage and quality?

### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?  
  
I expected a gap between quality and coverage. Furthermore, I expected that English speaking countries would perform differently than non-English native countries.   
    
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?  
  
I noticed that there was missing information in the datasets. Some countries might have less capacity for producing statistics and were therefore disadvantaged in the analysis.
    
1. What might your results suggest about (English) Wikipedia as a data source?  
  
English Wikipedia is biased since not all countries have the same level of English and therefore capability of writing high-quality articles in English. To perform a less biased analysis, all languages would need to be included.
    
1. What might your results suggest about the internet and global society in general?  
  
The internet can be a reflection of society and political structures. However, not every country has the same access to information technology. Therefore, information in the internet is biased and not all countries contribute to the internet and wikipedia in the same way.
    
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?  
  
Definitely, underrepresented countries and minorities can easily be disadvanteged. An AI works with the majority, therefore underrepresented groups or countries might be misclassified or not reflected.
    
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?  
  
If bias is uncovered and respected while creating and training the model, data science could even help to reduce systematic bias or point out inequalities. A good example woud be hiring processes. Currently, most hiring decisions are taken by humans. Humans are biased and therefore certain groups or people are being disadvantaged in the current system. An AI could help to solve this problem as it has the potential to correct human bias. However, it would need to be designed very carefully and with taking all potential bias in mind. It is important to create an AI which is less biased than the human-decision maker instead of creating an AI which simply reflects human bias.    
    
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?  
  
The datasets should not be limited to the English wikipedia. Additionally, the country statistics should not contain any missing information.  
