### Key Term Collection
- self-information
- Measures of Uncertainty
	- Entropy #_self-information_
		- Shannon Entropy
		- Differential Entropy
		- cross-entropy
	- Gini
- Units
	- bits/shannons
	- nats
- Kullback-Leibler (KL) divergence #probability


## TLS
- Why use entropy? What problem do they solve? What are the purposes of entropy?
	- Using the probabilities of each "class" (all class probabilities add up to 1.0), it calculates **uncertainty**. For example, if one class is absolutely sure that class A is the right answer, P(A) = 1.0, meaning that the rest of the probabilities are 0.0. Since it is completely sure, there is no uncertainty. However, if all class probabilites were equal, that implies absolute uncertainty, so the entropy would be the highest.
	- When is uncertainty applied? In classification problems and decision tree problems
- What is cross-entropy and entropy? How are they different?
	- Cross-entropy is $\sum{-y\log{\hat{y}}}$
	- Entropy is $\sum{-p\log{p}}$
	- The difference is that cross-entropy uses a guess for the probability in addition to the actual label 
- Why is cross-entropy used as opposed to just regular entropy as a loss function when using classification algorithms in machine learning? Why does this difference matter?
	- If the actual probability of a class should be really high, yet it is really low, it should matter a lot more. If entropy were to be used, then if the probability was the actual label, then there would be no variable to tweak that would minimize the uncertainty. If the probability was the prediction, then it wouldn't matter as much if it was really off. For example, if the label probability was 1.0 and the prediction probability was 0.5, that is a big loss!
		- However, if the label probability is 0.2 and the prediction probability was 0.9, there wouldn't be much of a loss, hence why entropy-based uncertainty is not good for regression problems and is much better for classification
- How does entropy work as applied in decision trees?
	- It helps decide how the decision tree chooses a feature to split on.
		- How? Entropy will measure the uncertainty if it chose to split on a certain feature $x_n$. Then, you will be left with a bunch of training examples that fit the results of the category. The ones that ultimately result in the same result with the category they are in are grouped together to form a part/whole probability for the entire "class" and fed into the entropy function to calculate the uncertainty (or impurity) of the feature if it were to split, and it does it for each new splitting node. By weighting each potential new node by how many examples there are and their uncertainties, a total impurity is able to be calculated for the feature. 
		- With decision trees, this is taken a step further with information gain: the new impurity score is subtracted from the impurity score of the last feature that existed that was already split on $IG = I_{0}-I_{1}$ 
- What's the difference between Gini Impurity and Entropy? Why use one over the other?
	- Gini Impurity is defined by $G=1-\sum{p^2}$
	- From the equation alone, you can tell that there is a similarity in approach between Gini Impurity and entropy. However, Gini seems to be computationally faster, but more linear
	- 
- Why isn't Gini Impurity used as a loss function if they are so similar?
	- If it WERE to be used as a classification loss function, it would go like: $1-\sum{y\hat{y}}$ 
		- Maybe it wouldn't even include the 1 as that could potentially be redundant
	- The reason it wouldn't be used as a classification loss function is because it does not penalize enough as entropy does. Both entropy and gini impurity are only really important in the domain of $[0.0, 1.0]$, which means that even though gini impurity is nonlinear, it is effectively linear as opposed to entropy when the label is true (y = 1). What does this imply? Entropy will prioritize correcting GLARING issues when the label is true
- How is cross-entropy different from KL Divergence?
	- KL Divergence is the difference between cross-entropy and regular entropy