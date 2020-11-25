# Summary Questions Redaing Book
"The Practice of Reproducible Research"
Kitzes, J., Turek, D., & Deniz, F. (Eds.). (2018). The Practice of Reproducible Research: Case Studies and Lessons from the Data-Intensive Sciences. Oakland, CA: University of California Press.

As I understood in case of reproducibility the repeating research team is using a dataset which the original research team also used and is providing in their publication. This could be for example time measured durring an experiment with test persons.  
Is it only called reproducibility if the repeating research team is using the data set of the original team (eg. the table with the time measured)? 
If I understood it correct creating the (same) dataset with applying the same methods and repleating the time measurement with diffrent 
users but the same demographic distribution is not reproducing the research but replicating? Because there are extraneous variables making the dataset of the repeating team different such as different psychological state of the test persons, different daytime, region etc. 

***

1. Why is this important ?

It did not seem relevant for me in the first sight. But I figured out the answer for me which I explain in the blog above.

***

I was wondering if there is a service or software that a researcher could use to get informed about the availability of his datasets. Through his career he/she might use different options to store research data. If the structure of the service changes, the service shuts down or the data just isn't accessible anymore, it would be good to know for the researcher get notified about this so he/she can perform actions.

***

1. Is it important to provide the full history of a data science project or is just important to keep the versions that were used for a publication? \
I assume it's only important to have the versions that were used for publications. Of course, if one uses a version control system like GitHub, it should be easy to offer the full history. On the other hand, there could be reasons (as stated above) to keep parts of the history secret (or even software artifacts used for a publication).

***

1. Making software reproducible can be very laborious. No problem for smaller projects, but when you have huge projects, I imagine it to be very time consuming. How can you make your work reproducible in larger projects with many people but still efficient?

***

I wonder wether the workflow on Jupyiter is suitable for larger projects. Is there a standarised procedure concerning this?

***

1. How does the need for reproduciblity differ when comparing academic research to in-company research or other fields? I imagine the possibilities to create completely reproducible research when researching user retention rates in a company for example are significantly smaller when compared to academic research, due to strict deadlines, the need for up-to-date data and limited budget. At the same time there may not be a need for the same degree of reproducibility compared to academic research.

If the degree to which you can implement reproducibility differs depending on the context, which "parts" of the reproducible workflow are best/ok to cut first?

***

* How often does a research project have to be reproduced in order for it's outcome to be accepted as valid ? 
* Does a single failed reproduction of the project neglect multible successful ones ?

***

1. What can be done to make sure that the data source (if it is coming from a different party) is sustainably available? Or is this not so important if we include the raw extrated data from that source into oure project? Because as in oure coding assignment it can happen that an API changes or disappears and even if we document and link to that API it might not me helpful in the future if the data source is not available anymore.

***

1. How can data scientists and social scientists collaborate more in the future to create unbiased and reproducable research?
1. Why is there only very little researcher who make their datasets and analysis publicly available?

***

Is there a better way to make reproducability or replicability easier while working with a large team, despite documenting each researchers work on its own?

***

1. I think the book generally talks about reproducibility and I assume it is not only oriented to data science. I can somehow understand the experimental setup in biology, physics. But what does it mean in data science? I am unsure if I understood it right, but the data analysis for me seems more like a data visualization. So there are actually no black-box algorithms behind that. I was wondering what is the experimental setup in our context/in data science context? Even if without following the reproducible workflow, will we get complete different plots?
1. My another question is about automation. I currently don't know how to reflect automation in my project and how to understand it in process. On slide 44 from the 2nd lecture, the guideline said "Document all operations fully, automating them as much as possible, and avoiding manual
intervention in the workflow when feasible.". What does it mean by "automation as much as possible"? Because of my lack of experience in coding, I wrote my dataframe operations seperately but not in nested functions, it is a source of violence of the automation rule?

***

There are many degrees of reproducibility. What degree is used for what purpose? I can image that developing software for a bigger company requires a very high degree of reproducility. But on the other side making sure a project is perfectly reproducible can be very time consuming and best believe that companys do not have the budget or the will to secure reproducible workflow. Therefore: what is considered a "minimum" reproducible project, that satisfies the criteria for reproducibility but also digs not too deep.
