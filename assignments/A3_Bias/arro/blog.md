# Assignment 3
> **Date:** 21.11.2020 - 11:54 AM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `arro` Arne Rolf
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  
_In at least 2-3 full sentences, answer the question "How does the video inform your understanding of human centered data science?"._
---
Introducing a semi or fully automated systems for decision making that should produce a more objective and unbiased outcomes than humans, is largely dependant on the data that is used. When using sensitive attributes that reflect social preexisting inequalities, the decision making algorithm might just reproduce structural discrimination such as classism or racism, which shouldn't be justified as a resembling of “harsh reality”.
Also, choosing strict thresholds in classifiers where a single percentage score can possibly change the outcome of someones life should not be take easily.
Additionally, a score generated from a dataset with a social bias does not consider personal aspects, such as motivation and soft skills.




### ❓&nbsp; Questions
_Using full sentences, list at least one question that this video raised in your mind, and say why it caused you to ask this question_

1. Was there someone in the AMS project who had doubts from a ethical standpoint about the data that they used?

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [Here](https://github.com/Arne117/A3-hcds-hcc-bias)

### Reflections and implications

In the third analysis step about the top 10 countries by relative quality, you could see countries with authoritarian leadership leading by quality content, which I assume is due their control of the country’s internet access. Some countries such as Uzbekistan, Saudi Arabia and North Korea completely blocked access for the population. Others might just try to control the quality of the article by suppressing criticism and other opinions that are contradicting to the government opinion. The bottom 10 countries by relative quality were small or emerging countries, where there was no quality article at all.


The top 10 countries by coverage where those with a correlating positive Press Freedom Index or just small countries with a low population, but with a high article count. Some of the bottom 10 countries might also have a correlation with the Press Freedom Index. For example, Djibouti has a score of 76.73 in 2020, which is just above China (78.48). A higher score means a lower degree of freedom for journalists.


What I have learned during this exercise was to use the pandas groupby and aggregate function. Chunking the API requests took a bit of time but was fairly easy in the end. I thought I also had to deal with asynchronous API calls, but I was relieved to see that the request library operates by default synchronous. I also wanted to implement the maximal allowed 4 parallel requests to the API, to speed up the process, but I didn’t find the time to do it. Plotting the results in for example a bar chart would have also been a nice addition but the exercise was time consuming enough by itself.


Question 1: This question just came up and probably can be solved with a quick google search but, what qualified an article to be categorized into the six classes. 
Question 2:


### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    That some countries take control over the articles about their own politicians. They control the media and press and can reference these articles when writing the Wikipedia article. 
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    As assumed above and in my reflection, countries with authoritarian leadership control the content of these articles or sometimes even block all request to Wikipedia for their population.
1. What might your results suggest about (English) Wikipedia as a data source?
    The English can contain data with a preexisting bias, which in this case roots in the government practices of the countries. They are controlling the access to Wikipedia itself and/or controlling the media and press on which the Wikipedia article are based on. 
1. What might your results suggest about the internet and global society in general?
    Without a free press and free speech of individuals that is granted by fundamental laws from the government of a country, it is difficult for mediums such as Wikipedia to reflect the reality due to the missing information and reports. As long as these countries control internet access and critics, one could only mitigate the situation by including content from articles written by journalist that operate in the hidden in this country.
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    Not now. I might add one later.
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    When comparing this dataset to the Press Freedom Index by countries, the opposite results (High article quality score in the Wikipedia dataset against a low Press Freedom Index) can support a correlation between these datasets.
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    One solution to mitigate this problem might be to add a correlating score with the press freedom index about the likelihood of the article being written by the government and not based a free press.