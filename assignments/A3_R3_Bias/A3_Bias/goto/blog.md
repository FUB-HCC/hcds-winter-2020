# 03 Exercise - Bias
> **Date:** 14.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `goto` Gorgin T.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective<br>
_Quelle: https://www.frontiersin.org/articles/10.3389/fdata.2020.00005/full_

### **🗨️&nbsp; "How does the article inform your understanding of human centered data science?"** _In at least 2-3 full sentences, answer the question_
The paper investigates the **AMS-algorithm** which should divide job-seekers into one of three groups, depending on their probability of both getting employed and for how long.
The paper stresses on the **importance of transparency of algorithms** that have public impact. Individuals will be supported according to to which group they were put it, hence this algorithm's public impact. The authors claim that the AMS-algorithm is missing out on this.
Amazon (_as a privately owned corporation!_) being unfair when scoring job-applications is one thing, to be honest. But personally, I was not aware that machine learning has already reached out to public realms such as official/governmental offices.
Yet still, risking a shit-storm, I found the quote of the AMS in the introduction to be of high relevance: _the system captures the “harsh reality” of the labor market by making realistic 'predictions_. So for me, this paper highlights the importance of hcds: There is certainly already an existing bias and injustice in the real world. Machine learning can not only capture it, but it can be amplified (as in the article I mentioned in the previous assignment, about judging on probation).


### ❓&nbsp; Questions
_Using full sentences, list at least one question that this article raised in your mind, and say why it caused you to ask this question_

1. Again, I wonder if it is even possible to create an algorithm free of bias and such. The argument that the AMS-algorithm simply incorporates the existing injustice of the job-market sounds valid: If all employers in Austria favour men, then the algorithm would give wrong output if it suggests hiring women?
1. Continuing the topic from the first question: Would it make sense to create some sort of preceding algorithm that shows something like  the probability of data being biased or creating unfair output?

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** [https://github.com/Nigrog/A3-hcds-hcc-bias]

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

_Mostly, I learned about Pandas. I had to look up a lot of stuff, e.g._ pandas sort _and such. As for the data, i found it hard to find errors. I believe I have done something wrong, for two reasons: The part where I gather data in batches of 50 takes surprisingly long and the resulting tables in the last task do not make so much in a sense, as I mention in the questions further down: Some countries are next to other countries that I did not expect. I guess I expected e.g. North Corea to lead at least one table. Any bias that can be taken into account with the data we have is wether an article name, standing for a politician, may be influenced in some way, e.g. targeted by spam-bots, or edited by "enemies". For that, we can get a hint about wether the article is of good quality or not, which already sounds a tad bit dependent on the judges opinion. About ORES, it says_ "some of the Wikipedians periodically evaluate the quality of articles" _so there is a source for bias to begin with.
Also, the size of the data made it difficult for me to see if I handle it correctly: My data-science knowledge is yet too low as to be really sure that these results actually are true.
_

_Your 350 words_

1. _Your question 1? - Not related to bias: If similar tasks are to come, can we get the results as we did earler (_ your plot should look like this _), so we know when we did somethig wrong?_
1. _Your question 2?_

### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    * _Unfortunately, I worked on the assignment before I went here to write any answers. I guess I would expect countries with tendencies of propaganda and/or suppression of free speech to be result-wise similar. _
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * _None. I believe I did something wrong. Take_ (4) Bottom 10 countries by relative quality _why would Luxembourg or Iceland be in the Top Ten here? Maybe the problem here is that some countries are, no judgment intended, less "important" when it comes to represantion on Wikipedia: **Maybe** the few people in Iceland simply do not care about Wikipedia. **Maybe** Iceland doesn't mess with other countries as much so other countries don't feel like editing pages for Iceland. This might mean that also the quality of articles is something that lacks of attention._
1. What might your results suggest about (English) Wikipedia as a data source?
    * _If it's the case what I wondered above, this ORES seems not to help in finding out anything. I may have gotten something wrong, though._
1. What might your results suggest about the internet and global society in general?
    * _Assuming again that what I said above is the case, then the internet society is highly unrepresentative. In my opinion that is definitely the case: The anonymity of the internet makes it an extralegal place. To most parts, it seems to be impossible to find out wether things said and done online are intentinally said and done the way they were. Already in "real" global society this is not as easy, think of false-flag operations. This is so much easier online._
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * _Yes, Wikipedia is made by people and therefore dependent on e.g. their mood or access to internet, censorship etc._
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * _Maybe, if you take doubts about the truth into account and then somehow categorise countries into groups regarding their freedom from censorship, access to internet, and such. _
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * _answer_

