# Title of your post
> **Date:** 14.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `mane` Marisa N.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  
_In at least 2-3 full sentences, answer the question "How does the video inform your understanding of human centered data science?"._

I have learned what enormous social implications a technical system can have and that these systems are permeated by man-made social values, norms and goals. It is very clear that data does not follow the principle of objectivity and neutrality, but can bring with it distortions that are a major challenge when it comes to implementing unbiased systems.


### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. Just as the system is biased, so are people. So how can we build systems that do not prepare and propose decisions that are biased, but rather point out to people their own bias? 

1. Who decides whether and how such systems may be used? The use of such systems can, as we see, have far-reaching consequences for people who themselves have neither control nor insight into these systems.

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [A3-hcds-hcc-bias](https://github.com/marisanest/A3-hcds-hcc-bias)

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

I have learned that it is not only important that Wikipedia has a large, covering number of articles on a particular topic, but that it is also important that these articles have a certain quality. So I took articles from each quality level and looked at them. I noticed that articles with the quality level "Stub" contain only very rudimentary information (e.g. https://en.wikipedia.org/wiki/Rita_Sinon), whereas articles with the level "FA" contain very detailed and well structured data (e.g. https://en.wikipedia.org/wiki/Don_Getty).

Furthermore, I have noticed that many countries have a high coverage of politicians that I would not have expected to find at the top of the English Wikipedia (e.g. Tuvalu or Albania) or countries further below that I would have expected to find at the top (e.g. Japan or India). Here the size of the population certainly plays an important role. A country does not necessarily have more politicians just because it has a larger population. Therefore, for countries with a large population it is more difficult to achieve high coverage with the method used in this exercise. It would be better to know how many politicians a country has or had in total to get a more representative coverage. I have also noticed that there are big differences between the coverage and the relative number of high quality articles. For example, some countries that are higher in coverage are lower in the relative number of high quality articles (e.g. Albania or Moldova) and vise versa (e.g. Korea, North or Uzbekistan). 

I was particularly surprised by the region of North America, which is only in 4th place in terms of coverage, but is in 1st place in terms of the relative number of high quality articles. This can either be factual and e.g. because there are more people in the English Wikipedia who care about the maintenance of articles about US American and Canadian politicians, whereas the total number of politicians is comparatively low and thus leads to a low coverage compared to the population size. On the other hand, bias caused by ORES could also lead to this result. This could happen, for example, if ORES was trained on data that take North American located as gold standart and thus these articles are rated better than those from other countries.

1. How diverse is the team behind ORES? 
1. What data has been incorporated into ORES? 
1. Which algorithm was used?


### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    1. Data bias to to the fact that english Wikipedia is edited by a specific user group which is biased by itself and thus generates biased data. As well as ORES can be biased already.
    1.  Sampling Bias due to the choosen data sources (one part of the data is very english centric-data because it comes from english Wikipedia and thus can be biased).
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    1. Processing Bias to to the aggregation of data to make it more understandable.
    1. Interaction Bias due to the specific choosen output (i.e. the resulting tables with only top/bottom 10 results).
1. What might your results suggest about (English) Wikipedia as a data source?
    The results indicate that there are large differences between the coverage and the quality of articles and that English-language articles are of better quality than those with a different geographical background.
1. What might your results suggest about the internet and global society in general?
    The results indicate a very Western-oriented society and use of the Internet. Although this is a very bold conclusion ;)
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    The data would be inappropriate, for example, if the aim is to build a system in which geographical location is used as a criterion to decide with what probability an article is or is not of high quality. 
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    Geeignet wären die Daten dafür, um ein System zu bauen, dass vorschläge an Wikipedia Nutzer macht, welche Artikel noch bearbeitet werden sollten oder in welchen Ländern oder Regionen potenziell noch Artikel zu Politikern fehlen. 
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    Other data sources could be added, such as Wikipedia versions in other languages. 
