# Assignment 3 - BIAS 
> **Date:** 23.11.2020 - 19:54 PM *(Due: 01.12.2020 - 03:00 PM)*
> **Name:** `frra` Franziska R.
> **Session:** [03 Exercise - Bias](https://github.com/FUB-HCC/hcds-winter-2020/wiki/03_exercise)   
----

## R3 - Reflection
> Article: Algorithmic Profiling of Job Seekers in Austria: How Austerity Politics Are Made Effective

### 🗨️&nbsp; "How does the article inform your understanding of human centered data science?"  
AMS would like to use an algorithm to evaluate job opportunities for the unemployed. For this, various variables are taken into account when assessing job opportunities, including gender. But also various other variables are criticized, e.g. to what extent the economic environment is taken into account.
One of the main problems is transparency, which, according to the paper, is not fully available.
From a human-centered perspective, the algorithm does poorly, because variables such as gender can produce discriminatory results, in addition there is also not much transparency. The algorithm is not an objective program, many value judgments and evaluations that should be discussed socially have been incorporated.

### ❓&nbsp; Questions

1. How can we prevent such a bias? When is system transparent enough?
2. Ethic comes from humans and not from machines. How can you check if data is biased? Can a data set ever be evaluated without prejudice so that there is no discrimination?

***

## A3 - Wikipedia, ORES, and BIAS

**Repository:** https://github.com/Francosinus/A3-hcds-hcc

### Reflections and implications

When I started this assignment I had to get used to the ORES API. Downloading the data was no problem and the preprocessing was not time consuming this time. But it took me some time to figure out how to use te API in an efficient way (my first approach took about 2 hours to get all the scores). But I made some improvements to the code and everything worked well and took not that much time to finish. 

The results:

The top three countries regarding coverage of articles with respect to the population are Albania, New Zealand and Norway. The population is rather small and a lot of articles exist, so it makes sense that these 3 countries are at the top. After filtering only the good quality articles Ireland, Bhutan and New Zealand are on top. So New Zealand not only has the best coverage of articles wrt. population, it also has good quality articles as well. Bhutan only has 2 good quality articles, but since population is small it is still on top. On the bottom of the coverage of articles wrt. population table there are several countries with few articles, but a large population. The same goes for the good quality filter results. On the bottom is Luxembourg with only 1 good quality article but about 600k residents. Looking at the countries on the top and bottom, it can be seen that for example New Zealand and Ireland which are on top are English-speaking countries in comparison to e.g. Luxembourg. 
After analysing the regions Africa and Latin America are on top regarding coverage of articles wrt. population. Looking at the coverage of good articles wrt. population Oceania and Europe are on the top. Oceania has a rather small population size n comparision to other regions. Australia and New Zealand belong to Oceania and are both English-speaking countries. The total of good quality articles for Oceania is 63, which is not a lot, but regarding to the population size the proportion is higher than for other regions. In addition New Zealand belongs to Ozeania and already has 13 good quality articles. 

In conclusion I can say that small countries or regions with a smaller population size are always on top and vice versa. So the population size matters a lot regarding to the proportion of articles. In addition the language plays an important role, English speaking countries commonly have more good quality articles. 


### Questions


1. What biases did you expect to find in the data (before you started working with it), and why?
    * Since english Wikipedia is the datasource, the data can be biased due to the fact that only english articles are used.
    * Thus I expected that non english speaking countries could do worse in the prediction
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * Inspecting the proportion of articles with respect to region e.g. it can be seen that that using the total amount of articles, Africa counts to the top. But     after filtering for quality articles, Oceania and Europe are on the top. This makes sense since in this areas English language is more often used than in Africa for example. Same goes for country.
    * This would be Publishing bias and selection bias I suppose 
1. What might your results suggest about (English) Wikipedia as a data source?
    *  English speaking countries articles are of better quality than those with a different geographical background. Thous it would be better to use Wikipedia with different languages and predict the quality. 
1. What might your results suggest about the internet and global society in general?
    * Don't know how the results could suggest something like this. 
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
    * It would always be biased if the geographical location is used to predict an outcome based on quality scores. 
1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
    * Maybe as a suggestion to edit bad quality articles. But still somehow inappropriate ("Hey your article in English sucks" ?).
1. How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?
    * Use Wikipedia in other languages as well. This would definitely take more time, since different ORES API models have to be used as well, but in the end the bias can be reduced. 
