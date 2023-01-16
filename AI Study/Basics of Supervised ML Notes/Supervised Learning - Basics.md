# Supervised Learning
**input -> output**
**x -> y**

Examples of applications:
- spam filtering:                          email -> spam? (0/1)
- speech recognition:                audio -> text transcripts
- machine translation:             English -> Spanish
- online advertising:     (ad, user info) -> click? (0/1)
- self-driving car:  (image, radar info) -> position of other cars
- visual inspection:  photo of product -> defect? (0/1)

Train model with right answers ((x, y) pairs) -> put a new input (x) for it to be able to generate a new output (y)

## Regression
Predict an output (out of *infinitely many possible outputs*) from an input
- Example: Least-Squares Regression
- Anything that predicts numbers is a regression model

## Classification
- **Predicts categories**
	- can be numeric (0, 1, 2) or non-numeric (cat, dog)
	- A classification model predicts discrete categories
- Different from Regression because there is a small, *discrete, finite number of possible outputs*. In the example below, there are only 2 types of outputs.
![[Pasted image 20220624194955.png]]
If 2 inputs were given and there were 2 possible outputs, it would draw a dividing line in the coordinate plane of the 2 inputs between 2 'regions' it classifies, such that belonging to region A yields one output and belonging to region B yields the other possible output. 