# Title of your post
> **Date:** 20.11.2020 - 18:00 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `chki` Christopher K.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the article inform your understanding of human centered data science?"  

Many software projects influence humans in some way. There a certain projects however that can have a huge impact. It is important to think about how the software will be used and what negative impact it could have on affected people. As a developer one has to be aware of bias and fairness during every phase of development. The paper sheds light on possible sources of bias and raises awareness for possible errors/mistakes. 

### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. Systems that are developed for decision making or for helping in the decision making process can lead to biased and unfair decisions. A system could be unfair but actually represents the real world correctly (for example becauese there is a systematic discrimination). Depending on a use case, can an unfair system be actually (more) useful? 
1. Is it the system's task to fight systematic discrimination or should these systems rather be a sign to take measures in the real world.
1. Since such a system can have a huge inpact on society, developers have a high social responsibility. Building fair systems (with a high impact) could actually be a way to fight unfairness in the real world. My question is, who decides what is fair and what is unfair? There are most likely many definitions and also a prevailing opinion in society. The latter could also be influenced (for examply by media) and follow ideological goals which might conflict with (objective?) definitions. 

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [Assignment 3 Repository](https://github.com/chrisk280/A3-hcds-hcc-bias)

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

I learned, that it is important to question the given data and to think about how the data could bias any results (in regard of the research question). This can be done in advance and it raises awareness during the process. Furthermore, I got to know ORES and gained hands-on experience with one of it's endpoints. This is not really big news, but the assignment reminded me that one should never assume that a given data set is correct and should always check for errors. For example there are erroneous entries for population in the data. \
My theories and expectations regarding biases are also explained in the next section 'questions' as part of my answers. In short, I think there might be a bias because we decided to only look at English articles. Furthermore, rows and countries were delete which might influence the big picture and the resulting tables only show a small part. For example, they do not show that there are way more than ten countries without any high quality articles (-> we cant say anything about the distribution). \
Looking at the results, many tables do not show obvious patterns at first sight. I think especially the 'Top 10 countries by coverage' and 'Top 10 countries by relative quality' contain some surprises. The former contains some countries with very few inhabitants and four countries from Northern Europe and the Baltics (which I assume have a good education and relatively few inhabitants). The latter table is interesting because the only European country is Romania but I expected more. \
I also found that there are more countries without any high quality articles about politicians in English than the table 'Bottom 10 countries by relative quality' can show. In my opinion, this fact makes the table rather useless. \
The table 'Regions by coverage' and 'Regions by relative quality' show that the two regions with the fewest articles/population, namely Asia and USA, have the highest rate of high quality articles. It also shows that the high quality article rate of the USA is by far the highest - around twice as high as Asia's rate.

In retrospect, I think it is a good idea to keep the columns in the tables that were used for calculating the column of interest (e.g. articles/population). They allow for a better interpretation of the results. For example, the rate of high quality articles of North Korean politicians is the highest. The number of total articles is of interest here, because for North Korea there might be only very few articles. These articles were probably edited a lot by people from western countries as well (keeping in mind the political situation in North Korea, it's political relevance and the media attention it got in the past). \
Unfortunately, I am missing the time to add these columns to the tables.

1. What do we do, if no license information can be found for a data source? I had a hard timing finding a license for ORES data and eventually gave up.
1. How to check for biases for systems like ORES? I can imagine that checking for biases can get very challenging if not impossible for systems of a certain size.
   In the case of ORES, we would likely need a large amout of articles that are objectivly rated by humans (an likely in different languages as well).

### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?

Since I don't really know how ORES works (for me it is kind of a black box), there could be a lot of biases introduced through the machine learning pipeline (sampling/processing bias, algorithmic bias). So the results might be biased because of biased prediction of article quality. The other bias that comes to my mind is the data bias. Apart from biased predictions, possible reasons could be incomplete data sets or missing attributes/information that might give more insights and shed a different light on the results.
I can imagine, that countries with English as their native language and/or countries with a good education system have higher quality articles in English language. If this assumption turns out to be true, the results might give a false impression of general article quality for certain countries.

1. What (potential) sources of bias did you discover or introduce during data processing and analysis?

    I think some data bias was introduced by dropping articles without a predicion or which had no corresponding country in the population data set. We might have dropped countries that could have made it to a top-10 or bottom-10 table and articles that were probably of high quality.
	
1. What might your results suggest about (English) Wikipedia as a data source?

   It depends on the research question. If we want to assess the quality of wikipedia articles about politicians for different countries, it might be unfair to use English articles only. Instead, assessing the quality of the article in the national language of the country might be more appropriate.
1. What might your results suggest about the internet and global society in general?

   It is difficult to draw conclusions regarding the internet or global society based on that data. One could probably see a relation between the power and wealth of a region and the rate of high quality articles. But I need a lot more information to be able to draw good conclusions. For example, it could be the case that the majority of high quality articles of Asian politicians was written by western authors.
   
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
   
   As stated before, the data might not be suitable for assessing general article quality (of articles about politicians or even other articles) for any country. 
   If ORES systematically rated articles differently depending on their relation to a certain country, it also could create problems. For example if it was used to rate the work of paid authors.
   
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?

   I think the data could be useful in many cases (especially if you are explicitly interested in the quality of English articles). For example, if the goal is to provide high quality articles for important German politicians in English, the data might help you to find articles which need to be improved. You could also use the data set to derive hyptheses (like: The amount of high quality articles in English is related to the ranking of the country in the PISA study). I think, the data can also be used if the research question is limited to countries with English as their national language.
   
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?

    Instead of getting predictions for English articles, one could retrieve predictions for articles written in the countries national language. Also, to get a complete picture one could try to get a complete list of countries. It is not trivial which politicians to choose from each country.
