# Assignment 2
> **Date:** 17.11.2020 - 02:05 AM *(Due: 17.11.2020 - 03:00 PM)*  
> **Name:** `xiyu` Xin Yu.  
> **Session:** [02 Exercise](https://github.com/FUB-HCC/hcds-winter-2020/wiki/02_exercise)   
----

## R2 - Reflection
> Book: The Practice of Reproducible Research (Chapter 2 and 3)

### Definitions
_Reproducibility and replicability_
_How does this relate to the definitions given in the lecture?_

* Definition from lecture:
>A research project is computationally reproducible if a second
investigator (including you in the future) can recreate the fnal
reported results of the project, including key quantitative fndings,
tables, and fgures, given only a set of fles and written instructions.
* Definition from Reading
>the ability of a researcher to duplicate the results of a prior study using the same materials as were used by the original investigator. That is, a second researcher might use the same raw data to build the same analysis files and implement the same statistical analysis in an attempt to yield the same results.

Both definitions mention that reproducibility is a matter of degree, rather than kind, which "means that identifying the factors that can relatively easily and quickly be changed can incrementally lead to an increase in the reproducibility of a research program". 

The lecture also adresses the important of FAIR data, which means the data has to be findable, accessable, interoperable and reusable. The FAIR data concept is not explicitly mentioned in reading but integrated into the workflow template and requirements of reproducibility.


### 🗨️&nbsp; "How does the reading inform your understanding of human centered data science?" 
_Describe in at least 2-3 full sentences._

The 2nd Chapter introduces fundamentals of the concept reproducibility and introduces different opinions on definitions of reproducibility(e.g. from ACM). It as well as differentiates reproducibility from other similar concepts: repeatibility.

The reading divide the assessment of three different board aspects and most of them (Availability and Automation) are what we do for our project in our repository , e.g.: documentation, license etc., to make our project open and reproducible for audience. 

The third Chapter gives the readers an introduction into project workflow which makes the concept into a more practical/doable data analysis process. Our project (Jupyter Notebook Assignment) also follows the general steps from data acquisition to data analysis. We also export/write inbetween outcomes (such as raw data in JSON, cleaned data in csv format) to present the outcomes after each stage. This process of our project is in accordance with the three main stages of reproducible workflow from the reading.

### ❓&nbsp; Questions
_List at least 1 question (full sentence) that this reading raised in your mind, and say why._

_My question doesn't based on reading itself. Since I first finished the Jupyter notebook and read the readings, I found something I may did it wrong in my project and my confusions raised by reading reflections._
1. I think the book generally talks about reproducibility and I assume it is not only oriented to data science. I can somehow understand the experimental setup in biology, physics. But what does it mean in data science? I am unsure if I understood it right, but the data analysis for me seems more like a data visualization. So there are actually no black-box algorithms behind that. I was wondering what is the experimental setup in our context/in data science context? Even if without following the reproducible workflow, will we get complete different plots?
1. My another question is about automation. I currently don't know how to reflect automation in my project and how to understand it in process. On slide 44 from the 2nd lecture, the guideline said "Document all operations fully, automating them as much as possible, and avoiding manual
intervention in the workflow when feasible.". What does it mean by "automation as much as possible"? Because of my lack of experience in coding, I wrote my dataframe operations seperately but not in nested functions, it is a source of violence of the automation rule?

***

## A2 - Reproducibility Workflow
_Briefly describe your experience using the reproducibility workflow._
The process is straighforward and the three stages are not different than general data analysis process. But the reproducibility workflow has its own requirements. 
My difficulties come mostly from coding itself, for example I had difficulties in data acquisition from APIs, parameters selection and write them in JSON files. Another difficulty is in data frame operations, I think it could be done more efficiently and decently, but I seems to do it too tediously with only basic codes.



### Final Wikipedia Page View Plot
_Add an image of your plot here and describe what you can see._ 🖼️ 
<br/>![Page Views on English Wikipedia](Page Views on English Wikipedia.png)


### Challenges
_Describe what tasks were challenging to you._

The API stuff and JSON File were the most challenging to me. Otherwise writing decent codes is also challenging.


_What was surprising, what did you learn?_ 😮 

I learned the reproducibility workflow by doing the project step by step from starting point and it was a really great practical takeaway of the academical concept from lecture. Otherwise I also learned some codes by googling while proceeding the project.

