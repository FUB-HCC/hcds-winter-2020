# A8 -Privacy and Security
> **Name:** `goto` Gorgin T.
> **Session:** [11 Privacy and Security](https://github.com/FUB-HCC/hcds-winter-2020/wiki/10_exercise)   
----

## Preparation
**Franziska Boenisch** works as a researcher at the Fraunhofer AISEC in industrial and academic research projects concerning private machine learning and data protection. She got her B.Sc. in 2017 and her M.Sc. in 2019 both at the FU Berlin. How she describes her research on her homepage is quoted below, as it is on point and I don't want to rephrase this:</br> 
_"My research interest lies at the intersection of Machine Learning (ML) and Data Privacy. Research has shown that trained ML models do not necessarily provide privacy for the underlying training datasets, as some attacks allow to restore (aspects of) the training data from the model parameters (e.g. model inversion attacks), or others allow to find out if a specific data point was included in the training dataset or not (membership inference attacks)._ [...]" <sup>1</sup>

- ##### Q1
- ##### Q2


## Summary
Boenisch gives an example as to introduce the relevancy of privacy aspects regarding machine learning: In good will, Netflix published data to developers and such, with the intention to let them work on "what else you might like"-recommendations. For this, they made sure to remove all personal data, however, it was possible to compare the data (such as "seen movies" or "given rating") with the database of IMDB and by doing so the entries from Netflix were identifiable.
She moved on with a brief explanation on how machine learning is works, how it gets trained and such.
In the next section, she moved on to talking about four methods how to attack ML systems, which are
- model inversion (reverse engineer the model)
- attribute inference (get attributes from the training data)
- membership inference (attacks aiming on wether an entry is within the dataset)
- model extraction (imitating the model (not sure about this))

After this, she tells some practises aiming to prevent ml systems from such attacks such differential privacy, which aims on obscuring the underlying data by adding some noise, this was explained by the average of people's height that would noticeably rise or fall when someone far from the average is added, so he/she might be identified and thus other knowledge gained in regards of changed outcomes.
Finally, she remarks that the ML system or its development may slow down, so there is a trade-off to be considered between privacy and performance.


## Mind Map
###### honestly I only added 2 points to the map as i am not sure about the techniques :(
![](https://raw.githubusercontent.com/FUB-HCC/hcds-winter-2020/main/assignments/A8_Privacy/goto/mindmap2.png)



## Question

- ##### The paper "_A Marauder’s Map of [...]_" suggests using open ML systems in regards to _gain_ security. However, I understood that it would mean more work to gain knowledge about it before being able to attack. I've might missed something but why is a black box _not_ harder to attack?

## Takeways

I found the aspect of adding noise interesting. I had guessed it would dilute the MLS' accuracy. (Maybe it does and it's what's ment with "it is a trade off")
</br></br></br>

1 https://franziska-boenisch.de/</br>




