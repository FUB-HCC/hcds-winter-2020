# Assignment 3
> **Date:** 23.11.2020 - 21:50 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `xiyu` Xin Yu.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  
_In at least 2-3 full sentences, answer the question "How does the video inform your understanding of human centered data science?"._

1. Regarding to human centered data science, the algorithm cannot be only reviewed and assessed from a technical view, since the algorithm is used for assiting human decisions and used for benifiting humans. Therefore, we should always keep its its social impact in mind.
2. The article also reminds me of last section concerning reproducibility since it is criticized in this paper that the "the document fails to explicate the exact nature of the data collection, cleaning and stewardship practices". This definitely reduces the algorithms reliability and credibility. Without a completely data understanding as well as concious data preparation, social prejudice can be easily learned and even exaggerated by not-well-designed algorithm.

### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. As mentioned in the article, the author criticized that the data collection and data cleaning processes are not well documented so that the data analytic process is not transperent and the algorithm may learn bias from data history. Combined with what we learned from the lecture, bias could be imitigated by conciouslly data preparation and increasing explanation as well as interpretability. But since human weselves all have somehow bias, to what extend can the algorithm/decision system REALLY "corrected" by human? 
1. Is there any evaluation metric for measuring bias? Should the algorithm be 0-tolerant towards bias or there is somehow acceptance rate? 
1. I assume we need to sacrifice some efficiency (or maybe even accuracy) for unbiased algorithm design, is there any tradeoff between the so-called "conflicting" goals?
1. How we differ bias and preference in a system? For example as a non-German native speaker I will be definitely disdvantaged when competing with a native speaker for a specific job such as journalist. I personally would not take it as bias/discrimination, it is just a specific preference for specific background/competencies. But still the algorithm outcome maybe considered as unfair if we use the statistical measure. In this case, what will we see as preference; what will we see as bias? Is there any discussion on this issue in academic/practices?

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [A3-hcds-hcc-bias](https://github.com/yuxin16/A3-hcds-hcc-bias)

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

_Your 350 words_

* Learned:

1. From Practical View (Programming):
    
    I get more familiar with API usage and dataframe operations. I also get more acquintanced with this reproducible workflow. It surprised me of how long it could take if I sent query based on single rev_id (unfinished in 4 hours). 

2. Regarding Project Itself:

    I was wondering of the validity of measurements and if the measurements are convincing to some extent.
    The project for me, personally, is unclear in its purpose. Even though I knew that we would like to compare countries based on their coverage as well as relative quality, I don't know what the measures stand for, or in other words, what they can proof? I think if the research question of this project made clear at the beginning of the project, we can review our project/workflow in a more reflective way.

    The results also surprised me by showing some countries in the top rank which I have never heard of (e.g.Tuvalu raked on top for top 10 countries by coverage).

    Since the machine learning algorithm used by ORES is unclear (or I haven't found it) as a black-box, the trustworthiness of this algorithm is also under doubt.

    I was also suprised by not seeing United States on the country list, since the dataset is from english wikipedia. Some countries with other official languages could be disadvantaged in this analysis but still the United States doesn't appear on the final list.

3. Theoretical Points regarding Bias

   As mentioned in Point 2, algorithmic bias may exist within the black-boxed algorithm. Sample bias can also be considered in this project since the sampling is highly relevant to research questions. The dataset contains only pages in politicians on english wikipedia, so I was also wondering if there is any data collection bias based on the chosen language and platform.  

_My Questions_

1. My first confusion is regarding the analytical purpose of this project. I am confused why we calculate those measures? For discovering political interest in different countries/regions? Then I actually doubt English Wikipedia as a good data resource becasue even though english is popular, it is not official language in most part of the world. And there are some countries they have their own "wikipedias" and may not use wikipedia quite often. 


### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    * Algorithmic Bias introduced by machine learning algorithm used in ORES scoring. The assessment of quality is unclear, if the quality assessment is based on grammatical proficiency, articles written/edited by non english native speakers could be disadvantaged in this scoring system.
    * Activity Bias: Population bias and bahavior bias are the my expected bias for this project. The dataset is retrieed from edited pages on english Wikipedia so there is a possibility that the people who don't speake English and/or doesn't edit Wikipedia are kind of "ignored" in this analysis. 
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * Data acquisition. The raw data on downloaded from online source and the data collection details is not 100% clear. If the data was collected for other researc purpose, it may create bias for out analysis. 
1. What might your results suggest about (English) Wikipedia as a data source?
    * It is really hard to evaluate a data source without specifying the research purpose. I still consider it as a good data source with the largest online wiki database of global coporation. However, it has its own limitations. By using wikipedia as a data source, we need to carfully formulize our research question and consider its restrictions beforehead. 
1. What might your results suggest about the internet and global society in general?
    * Honestly speaking, I don't think my resuls can suggest anything about the internet and global society, especially **IN GENERAL**.
    I don't think this project is valid for this purpose a all.
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * **THIS** research, actually. We can assume that our research purpose is to map the public interest in politicians, this project can be heavily biased based on discussions in previous questions. 
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * Yes. The research needs to be restricted to english wikipedia users. The data source may be suitable for mapping the public interest in politicians under Wikipedia's online english community.
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * (1) We can include more discussion supported platforms such as Youtube and Twitter; (2) We don't have to limit to english versions; (3) For contries with their own online communities, those platforms should be calculated in; (4) Consider the accessability to several platforms in certain areas (e.g. Youtube/Twitter in China). 
