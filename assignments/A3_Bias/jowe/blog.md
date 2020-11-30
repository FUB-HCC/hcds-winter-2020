# Assignment 3
> **Date:** 23.11.2020 - 21:28 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `jowe` Jonas W.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  
_In at least 2-3 full sentences, answer the question "How does the video inform your understanding of human centered data science?"._

When creating any type of computer system it is neccessary to view the system as the complete socio-technical system it is, instead of only a technical one, which may be completely correct or calculcated. It is important to think about and discuss the possible implications any system might create when introduced into the context in which it is supposed to be used, as well as any current factors coming from this context which might have influenced the creation of said system. 

### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. While the authors raise very valid points about specific problems of the AMS Algorithm I am unsure whether I agree with the points they raise about whether a "workfare" state is morally good or bad or whether putting job seekers in a category of low chance of employment may be a self fulfilling prophecy. While these points are surely worth discussing, the question it raises for me is, if every person in every position should be responsible or moraly obligated to break biased structures in their society. In my opinion, whether the "workfare" state is the "right" state structure should not be a question influencing the creators of descriptive algorithms like the one at the AMS in their work. The goal of the algorithm was to predict the chance of a specific applicant to get hired in a given timeframe in the current society. If the system, which the algorithm describes is biased against groups of people, shouldn't the algorithm display that? It is objectively wrong to not hire applicants based on factors like age, gender, etc. but in my opinion the authors mix up their valid criticism of the inner workings of the algorithms with a system critique which may not have a place in this discussion but should and must be continued in another seperate place. Whether this is the right approach and leads to actionable results rather than stopping the use and improvements of such algorithms due to systematic problems which aren't influenceable in the same timeframe and by the same people, is a question worth thinking about and discussing, in my opinion.

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [Repo](https://github.com/jonas-weber/A3-hcds-hcc-bias)

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.


Since this exercise was a lot less guided than the previous ones, it deepened my pandas understanding. I also got introduced to the ORES API which was very interesting as well as easy to use to me. While only some of the data seems to hold any properly interpretable information, the results had some quite suprising points, like North Korea having the highest rate of high quality articles. I think the main bias which exists, stems from only including english Wikipedia entries. Especially when looking at countries with limited education, there may be a lot more articles, as well as higher quality ones, when including the countries respective language. Since a lot of countries english education is quite limited or only present in specific subgroups of the population, the data could also be heavily influenced by educated young people or even users from english speaking countries, writing articles about foreign politicians, which would stop the dataset from providing any useful information about the context its trying to research.
Besides this bias, this data was also problematic since the country names weren't standardized so quite a lot of countries are missing entirely and the population numbers were wrong for some countries which makes any useful results difficult when starting with data containing mistakes. So overall this exercise reminded me again that, as learned in the lecutre, it is important to not only look at the data itself, which may contain mistakes heavily influencing the results, but also its origins and determining whether this data can even produce any results worth interpreting without additional data or changes.

### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    * I expected there to be some form of bias against countries with lower quality education and/or internet access, since, in my opinion there is a high chance for that to happen when working with any form of international internet data.
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * As said above, my main source of bias would be limiting the data to english articles.
2. What might your results suggest about (English) Wikipedia as a data source?
    * As mentioned in the lecture, english Wikipedia is mainly used by male, western users. This is an important point one has to keep in mind when using any of Wikipedias data to analyze anything in a international context.
3. What might your results suggest about the internet and global society in general?
    * Same, as question 2. Countries with poorer education resulting in lower quality english, as well as worse internet access, are heavily underrepresented in both the internet and global society in general.
4. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * A possible research situation could be trying to determine the quality of knowledge one countries inhabitants have about their politicians by looking at the article quality rate. Since only english Wikipedia was used, there's a possibility that a high amount of ones countries articles are written by westernes, thus not representing the countries population at all.
5. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * I think the only situation where this data can be used without adding a lot of other data to it, is when limiting it to only english speaking countries. This would get rid of the main bias I found and may still hold some interesting findings about the countries.
6. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * Using the given countries respective language instead of english when looking at the articles and their quality would potentially correct the bias and make the data more useful for its intended purpose.
