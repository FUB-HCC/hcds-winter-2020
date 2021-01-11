# Summary Questions - Ebook Molnar

R4 Questions

1. I am not sure if I understood the categorization of an *Intrinstic* method correct. 

It is meantioned that the intrinstic method is archived by restricting the complexity of a model. By reading this I understand that intrinstic interpreatability is possible when choosing a simple model (e.g. linear regression). 

It is also mentioned that for intrinsically interpretable models the models internals (e.g. the learned weights) are inspected and tried to be explained. So do I got it right? Is the a criteria for an interpretation method to be characterized as *Intrinsic* that it is used for models with simple complexity and where the models internals are viewed?

**Why:** ...
I am asking this because I understand that per this definition Convolutional Neural Networks falls also to the *Intrinstic* interpretable models because of its learned weights and biases. But when I am thinking of some deep CNN's I cannot imagine these to be less complex.y.

***

1. Can we solve complex problems with only intrinsic machine models?

**Why:** Since we restrict the complexity of the model I asked myself if we can solve complex problems where maybe complex models are better suited.

***

1. Is the method "Intrinsically interpretable model" meant to dissect the model layers to be able to look at each individual outcome? If so, is the model to be analyzed recreated as a new second model with the same layer parameters but with the learned weights from the first model?

***

1. Can post-hoc methods ever achieve the degree of interpretability/transparency that intrinsic models offer?
1. With regard to the last question: I think that the necessary degree of interpretability depends on the use case. There might be cases in which simplistic models are too weak for modeling complex situations. So at some point, I assume, we are dependent on methods for interpretability. How do we assure high interpretability for complex models in sensitive application scenarios? Can these methods create enough transparency and trust?

***

1. Is there a "best practices" when trying to achieve good results but also model interpretability? 

***

1. What came to my mind is that it is quite exhausting when a book has no "golden thread" which it seems not to have here.

***

1. How commonly used are these methods to achieve interpretability in actual research?

***

1. How much precision is lost when the interpretation tool in model-agnostic ?

***

1. Is there already a known interpretation method for each well known, but not intrinsically interpretable machine learning model (e.g. GANs, RNNs, etc.)?
**Why:** The proposed approaches sound great but when it comes to practice and to really complex models, how can we make them interpretable?
1. How can we asses which model we should use when we talk about interpretability?
1. Is there a threshold, when it comes to a trade-off between a more accurate and a intrinsically interpretable model?
1. Why should we use a more complex model in the first place when we later on translate this model to a intrinsically interpretable model for better interpretabllity?
**Why:** These three question arise because I am curious about which model should be choose in the first place and which model is a  "good"/"proper" model for specific cases.

***

1. I understand the necessity of interpretability, but I wonder if this is not more like looking for a needle in a haystack, since there is no "one-size-fits-all" technique to measure?


**Why:** There is no real consensus about what interpretability is in machine learning. Nor is it clear how to measure it. The only way to appriximize the measurement of interpretability is through different level of evaluation (e.g. application, human and function level evaluation). In addition to that, these levels are only simplifications of other levels, so basically there is no way to include all three aspects. So this reminds me a lot of Googles "auf gut Glück" search, where you try your luck and hope to find appropriate results.

***

1. I am wondering in which case which method should be used? Or is a combination always best?
**Why:** The text left me with open questions regarding the application. I would have liked to see concrete examples for better understanding which method should be used in which case

***

1. What are possible ways to rework existing models towards being unbiased?

***

1. I am still a little bit confused on difference between explanations and interpretations. In the chapter 2.2 (or generally chapter 2), it seems that the author use them as synonyms. <br>**Why:** I have read some general papers on XAI which describes interpretability as intrinsic explanability, therefore, it seems that interpretability is subconcept of explanability. I am unsure how to clearly differentiate them apart from each other or they are actually the synonyms. 

1. Is there any difference between interpretability or interpretation methods for parametric and non-parametric learning models? <br>**Why:** This question is interesting for me because some interpretation methods are based on parametric statistics, and I am wondering if there is something we need to consider of when choose an interpretation method. 
