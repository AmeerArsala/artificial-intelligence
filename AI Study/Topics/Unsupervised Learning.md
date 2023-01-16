## Prestudy: Keyword Collection + basic groups
- **Clustering**
	- DBSCAN
	- Expectation Maximization (EM)
		- K-Funcs
			- K-Means
			- K-Medians
	- Louvain Clustering
	- Hierarchical Clustering
		- BIRCH
		- Agglomerative
		- HDBSCAN
	- Affinity Propagation
	- Spectral Clustering
	- Mean-Shift
- **Anomaly Detection**
	- Gaussian Mixtures
		- Normal Distribution = Gaussian Distribution
		- Bayesian Gaussian Mixtures
	- Density Estimation
- **Dimensionality Reduction**
	- Projection
		- PCA (Principal Component Analysis)
		- LDA (Linear Discriminant Analysis)
	- Manifold Learning
		- Locally Linear Embeddings (LLE)
- **Association (Rule Learning)**
	- Apriori Algorithm




## TLS: INQUIRY-BASED LEARNING
**Reminder: questions must be open-ended and EXPLORABLE and THOUGHT PROVOKING**
### Session 0
- Why is Clustering Important? How can it be applied?
- Why is Anomaly Detection Important? How can it be applied?
- Why is Dimensionality Reduction important? How can it be applied?
### Session 1

- What's the point of clustering?
- How does anomaly detection work?
- What is the application of Density Estimation and how does this relate to Anomaly Detection?
- How does selecting the number of clusters differ in K-Funcs and Gaussian Mixtures? 


#### Clustering
##### K-Funcs
- Why does K-funcs clustering have a high time complexity when the data isn't in a clustering structure?
- How does the K-Means model know which cluster is the best when fitting?
- How does Accelerated K-Means avoid many "unnecessary distance calculations"?
- Why would I want to use mini batch K-Means? 
- How do you know what the optimal number of clusters is? Is there anything else other than elbow method and use case?

- What is the connection between the probability density function (PDF) and radial basis function (RBF)?

##### DBSCAN
- What is DBSCAN, what is it used for, and how does it work? Does it have anything to do with a radial basis function? Is this density estimation?
- How does DBSCAN differ from K-Means if they're both clustering?
	- *K-Means is focused on center*
	- *DBSCAN is focused on density and individual instances to create an overall neighborhood*
- What would be an application where K-Means is better than DBSCAN?
- What would be an application where DBSCAN is better than K-Means?

##### Expectation Maximization
- What exactly is Expectation Maximization (EM)? How do Gaussian Mixtures utilize Expectation Maximization?
- How does EM work?

#### Gaussian Mixtures
- For Gaussian Mixtures, why isn't just a regular Gaussian (Normal) Distribution used? Why are they mixed? That is, what is the point of using a a mixture of Gaussians rather than just a single (multidimensional) one for the dataset?
	- *Each Gaussian Distribution represents a cluster*
	- *A multidimensional Gaussian Distribution (per feature) IS used*
- Why do we need a generative process? 
- Why is each x sampled RANDOMLY? Why can't it just be a 1:1 conversion?
	- *In order to representatively draw from all populations/clusters*
- How does a GMM learn what is "normal" for Anomaly Detection?
- How does the "generation" work in a GMM? Is the sampling just from the weighted randomly chosen population's distribution?
- How does sampling from a normal distribution work?
- How does a GMM perform Density Estimation?


### Session 2
- What separates EM algorithms from DBSCAN in clustering? 
- Why would you use EM as a form of clustering over K-Means? 
- If possible, how would clustering handle sequential data?
- How could clustering be used to process images through Region Proposals?
- How do Gaussian Mixtures learn "what is normal"?
- How does Semi-Supervised Learning work specifically?
- Why is label propagation important?
	- because it allows us to label a bunch of unlabeled examples using stereotypes
- What's the point of active learning? How does it improve the model and what makes it better than any possible alternatives?
- When should I use Agglomerative Clustering as opposed to Expectation Maximization? 
- How do we know when to select between BIC and AIC?