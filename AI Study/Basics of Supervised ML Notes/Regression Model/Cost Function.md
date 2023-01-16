# Linear Regression with One Variable
In order to implement Linear Regression (see [[Linear Regression Model]]), a ==**cost function**== must first be defined. This is a key part of Supervised Learning (see [[Supervised Learning - Basics]])
$$
\begin{gather}
f(x) = wx + b \\
f_{w,b}(x)=wx+b \\
\hat{y}^{[i]} = f_{w,b}(x^{[i]})
\end{gather}
$$
- `w, b` are known as the **parameters** (variables you can adjust during training). Also called **coefficients** or **weights**

$$
\begin{gather}
\textbf{Goal: } \text{Find } w,b: \hat{y}^{[i]} \text{ is closest to } y^{[i]}\ \forall \ (x^{[i]}, y^{[i]}) \\
\\ \text{where:} \\
\hat{y} \text{  is the estimate} \\
y \text{ is the target (the actual data point)} \\
m = \text{number of training examples} \\
\therefore \text{error = } (\hat{y} - y)
\end{gather}
$$
## Cost Function
- Most common cost function for linear regression is the squared error cost function
- Computed as the *average of the sum of the squared errors*
- By convention, machine learning engineers divide by 2 to make calculations neater
 $$
\begin{gather}
\textbf{Squared Error cost function} \\
J(w,b) = \frac{1}{2m} \sum_{i=1}^m{(\hat{y}^{[i]} - y^{[i]})^{2}}\\
\downarrow \\
J(w,b) = \frac{1}{2m} \sum_{i=1}^m{(f_{w,b}(x^{[i]}) - y^{[i]})^{2}}\\
\downarrow \\
J(w,b) = \frac{1}{2m} \sum_{i=1}^m{((wx^{[i]}+b) - y^{[i]})^{2}}
\end{gather}
$$
- In terms of the cost function, the goal up above means we want to **minimize J(w, b)**
$$
\text{Since } J(w,b) > 0 \ \ \forall \ (w,b) \in \mathbb{R}, \text{ we want } J(w,b) \text{ to be as close to 0 as possible}
$$ ![[Pasted image 20220628181105.png]]
![[Pasted image 20220628184541.png]]

### How do we minimize the Cost Function?
By [[Gradient Descent]]
