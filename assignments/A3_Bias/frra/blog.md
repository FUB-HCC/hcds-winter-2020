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

**Repository:** https://github.com/Francosinus/A3-hcds-hcc/edit/main/blog/blog.md

### Reflections and implications



### Questions


1. What biases did you expect to find in the data (before you started working with it), and why?
    * Since english Wikipedia is the datasource, the data can be biased due to the fact that only english articles are used.
    * Thus I expected that non english speaking countries could do worse in the prediction
1. What (potential) sources of bias did you discover or introduce during data processing and analysis?
    * Inspecting the proportion of articles with respect to region e.g. it can be seen that that using the total amount of articles, Asia counts to the top. But     after filtering for quality articles, Europe is on the top. This makes sense since in Europe English language is more often used than in Asia. Same goes for country.
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
    * Use Wikipedia in other languages as well. This would definitely take more time, since different ORES API models have tio be used as well, but in the end the bias can be reduced. 
