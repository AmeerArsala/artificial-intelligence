# How Machines Learn
#### In order to get the "correct" answer, we want to minimize the cost function
Below is a cost function visualized.
**We want to change w and b such that (w, b, J(w, b)) is the minimum value of the cost function J(w, b)**. In other words, we want to find the **absolute/global minimum** of the cost function J(w, b)
 ![[Pasted image 20220628184541.png]]

This essentially boils down to:
1. Choose a good starting point of (w, b, J(w, b))
2. Find the local minimum (a good starting point is one that leads to a local minimum that is also the global minimum)

# Gradient Descent
The most popular way to do this is by gradient descent.

$$
\begin{gather}
\text{3 properties of the gradient} \\
1.) \ \ \overrightarrow{\nabla{J}}(w, b) \text{ points in the direction of the max rate of change of J at (w, b, J(w, b))} \\
2.) \ \ ||\overrightarrow{\nabla{J}}(w, b)|| = \text{ the max rate of change of J at (w, b, J(w, b))} \\
3.) \ \ \overrightarrow{\nabla{J}}(w, b) \perp \text{the level curve/surface at level J(w, b)}
\end{gather}
$$
$$
\begin{gather}
\text{Since these properties are true, we can conclude that }-\overrightarrow{\nabla{J}}(w, b) \\
\text{corresponds to the least (most negative) rate of chance (it is literally the opposite direction)}
\end{gather}
$$
- This means it will point towards the minimum

$$
<w_{i+1}, b_{i+1}> \ = \ <w_{i,}b_i> -\alpha\overrightarrow{\nabla{J}}(w_i, b_{i)}
$$
Where alpha = step size = learning rate

**This *will* take you to the local minimum or close to it**


## Terminology
**Batch Gradient Descent**: gradient descent, but it looks at every example in the entire training set at every step