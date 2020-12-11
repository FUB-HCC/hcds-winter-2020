# Title of your post
> **Date:** 14.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `alsc` Alexa S.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Video: The Trouble with Bias - NIPS 2017 Keynote - Kate Crawford #NIPS2017.

### 🗨️&nbsp; "How does the video inform your understanding of human centered data science?"  

My main takeaway from the article is that biases can't always be split up into different categories, to later be used by a program, to calculate a possible discimination tendency. As was mentioned in the text the amount of discrimination a woman of a certain heritage encounteres does not directly correlate to the discrimination a man with similar heritage might encounter. The data therefore implies that the amount of discrimination depends on all the different characteristics combined, rather than the sum of the discrimination due to certain characteristics.

For instance, an arabic woman without a university degree might be discriminated by 60% (due to her characteristics: female 20%, arabic 20%, no degree 20%), but that does not imply that an arabic woman with a university degree will be discriminated by 40%.

### ❓&nbsp; Questions

* How much more bais is an reasonably well implemented algorithm (meaning it doesn't overly discriminate against large groups e.g. woman) compared to humans doing the same job and should a certain level of bias be acceptable in an algorithm, since it might at least be less bias than it's human counter part would be ?

* How much easier might it be to attack bias within alorithms, compared to attacking bias within the mindset of the many workers, that would otherwise do the job ?

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** `<add link to our repo here>`

### Reflections and implications

Write about `350` words, reflecting on what you have learned, what you found, what (if anything) surprised 😲 you about your findings, and/or what theories you have about why any biases might exist (if you find they exist). Please also include any questions this assignment raised for you about bias, Wikipedia, or machine learning.

One of the rather obvious takeaways to me has been how crucial the relative value of a lot of these statistics is. Not taking this relativity between a value for a statistic and the overall size (population) of the country into consideration might lead to very different results. 

Also it was rather surprising that even in a very well established and widely used world language such as english, the amount of quality articles drastically declines, when looking at third world countries. This raises my first question, which is whether the people in third world countries just don't write articles about their local or regional topics in english, or rather they don't write wikipedia articles at all. This would obviously create great bias, even if one would combine the english data with data from other languages. Further this could point to the issue that either the people in those countries don't have access to the technology to write those articles, or that they don't have the education or even time to worry about something that is not important to survive. 

In addition there could be information sites other than wikipedia, that might be more popular in other countries, so just taking the numbers from wikipedia (at least without research whether there is such a site) could also produce missleading results.

The problem, that people are mostly interested in topics that are close to themself, or that they can relate to, causes people from different geographical background to have different amounts of knowledge and therefor give different amounts of emphasis on certain topics. As an example, since their are more people in america that know about the generall american history than there are proportionally in the rest of the world, there will be more well written articles about those topics in english. This causes students from america who want to educate themselves on those topics to have more sources at hand, than a student from egypt who doesn't speak english. Therefore the level of education about topics stays more regional, especially when looking at other languages like italien or greek, which are not nearly as widespread as english. 

This concludes my reflection and raises my second question: "Would knowledge about regional topics be more widespread if it wasn't mainly available in the local language, or are people just generally more interested in topics that are closer to their life and history?"

### Questions

Pleas answer the following questions with at least 2-3 sentences each.

1. What biases did you expect to find in the data (before you started working with it), and why?
    * I expected to see baises against poorer countries and regions.
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * I found that the quality of the articles greatly depends on the economical state the country or region is in, which causes North America and Europe to be at the top of the list for article quality.
1. What might your results suggest about (English) Wikipedia as a data source?
    * It shows more results for countries that speak english and are overall more developed.
1. What might your results suggest about the internet and global society in general?
    * It suggests that people are generally more interested in topics that are geogrphically and culturally closer to them.
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * It might suggest that there are less people in undeveloped regions, that care about politics and therefor a program might label them as less educated.
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * For doing research in North America where the amount of available, good quality articles about a topic actually reflects the amount of topics that are important enough, to require such an article.
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * A researcher add data from different wikipedia languages and take the mean of represented articles and their quality.
