## Machine Learning Engineering
- How should you go about selecting a model in terms of the training set, test set, and cross validation set?
- When will a model have high bias? High variance? Just right?
- How do you choose the parameter lambda in regularization using cross-validation?
- What are the values of J_train and J_cv as functions of a polynomial degree d?
- What are the values of J_train and J_cv as functions of the regularization parameter lambda?
- Explain why the 2 graphs from the 2 previous questions are mirror images of each other.
- Name a few examples of a baseline level of performance and explain how they relate to J_train and J_cv.
- In general, why is J_cv > J_train?
- Describe the ML Development process
- Describe the error analysis process
- What is the difference between data augmentation and data synthesis? (compare and contrast)
- What is transfer learning and how does it work?
- How does transfer learning impact a machine learning project?
- Think of a use-case for transfer learning
- How does orthogonalization characterize the ML development process?
- Why is learning fast when the ML model is worse than human-level performance?
- When does the selection of a measure for Baye's error matter when it comes to Bias-Variance analysis?
- When is it not appropriate to use transfer learning?
- Why can't softmax be used in multilabel classification?
- How do you learn in multitask learning when the training set has some y's that don't label certain  outputs (example: in an image with a tree, a cat, and a fire hydrant, a y in the training set only has labels for the tree and cat)?
- What is early stopping and how can you take advantage of it? Why is this important (as applied to both overfitting and underfitting)? 
- How does early stopping tie together optimizing the cost function and optimizing generalization (bias and variance) as a form of regularization?
- Describe 2 ways to normalize inputs. Why would you normalize them?

## Classification
- Describe the confusion matrix for binary classification.
- What is the difference between precision and recall?
- What is the F1 Score and how does it work?
- Think of a situation in which a model may have high precision but low recall.
- Think of a situation in which a model may have low precision but high recall.
- How does the ROC curve work?
- Describe the ROC curve of a good model.
- When should you use precision recall curve as opposed to the ROC curve?
- What is the difference between One versus One and One versus All classification? (compare and contrast)
- Hard Margin Classification vs. Soft Margin Classification
- What should you do when dealing with categorical features in classification? Answer in the context of a Decision Tree and a Neural Network.
- How does Multilabel Classification differ from Multiclass Classification? How is each implemented?
- What is Multioutput Classification?

## Support Vector Machines (SVM)
- What is the kernel trick? Describe it

## Decision Tree
- How to choose what feature to split on at each node in a Decision Tree?
- How does choosing a feature to split on differ between a Decision Tree Classifier and a Decision Tree Regressor?
- Compare and contrast the advantages of Decision Trees and Neural Networks

## Ensemble, Random Forest
- Soft Voting vs. Hard Voting. How is this related to Ensemble Methods?
- Random Patches vs Random Subspaces
- Bagging vs. Pasting. Compare and contrast. Why should you use one over the other?
- Why is the Random Forest Algorithm more efficient than a regular DecisionTree Ensemble?
- AdaBoost vs. Gradient Boosting
- XGBoost

## Neural Networks
### Activation Functions
- How does the activation function relate to the cost function?
- Why is ReLU faster than Sigmoid?
- Why do we need activation functions?
- How does the Softmax activation function differ from typical activation functions?

### Deep Learning Engineering
- Wide vs. Deep Neural Nets. What are the advantages of each?
- How does the Adam Algorithm differ from the Gradient Descent algorithm?
- How does dropout regularization drive down the weights?
- Describe gradient checking. Why is this useful?
- What causes vanishing/exploding gradients and how can you avoid this problem?
- How can the mini batch size as a hyperparameter be used to make gradient descent converge faster?
- How do momentum and RMSprop combine to create the Adam algorithm?
- What does Batch Normalization normalize?
- How and why does Batch Normalization make bias terms (b) obsolete when used?
- How exactly does BatchNorm change a layer? What are the effects?
- When does an end-to-end deep learning approach work? How does it compare to a more hand-crafted approach? What are the pros and cons of each compared to each other and when should each be used?

### Convolution Neural Networks (CNNs)
- Describe the convolution operation when talking about a D-Dimensional Frame and C channels of the input and kernel/filter. Also factor in striding and padding.
- What is the relationship between (n_x)^[l] and (n_x)^[l - 1]  as well as (n_y)^[l] and (n_y)^[l - 1]?
- Why is Pooling important? Why is a CONV layer typically followed by a POOL layer? 
- How would you rank LeNet-5, AlexNet, and VGG Net? What is the common theme that makes 1 better than the other? 
- In what way is a ResNet better than a regular neural net? Why do skip connections make ResNets better? 
- What is the use of a pointwise convolution (1x1 convolution)? 
- Why is a 1x1 convolution often called a "network within a network" ?
- What is the idea behind an inception network? How does it work?
- What makes a depthwise convolution different from a regular convolution? 
- What is the advantage of a MobileNet? How does it achieve this? 
- What is the y vector in classification with localization and what is it's loss function?
- Why does the convolutional implementation of sliding windows solve the high computational cost problem? 
- Why is translation invariance important and how does it relate to a big-picture view? How does max pooling capture this?
- How do you choose the coefficients for each layer for the style cost function in Neural Style Transfer? How do you do it such that the generated image strongly follows the style of the style image?
- What are the sectors of the U-Net architecture and what is the U-Net used for?
- How does a transpose convolution work? 
- How is the stride for a transposed convolution layer different from the stride of a regular convolution layer?

### Recurrent Neural Networks
- When is EOS token useful?
- What role do gates play in gated cells (why do we need gated cells to begin with?), and how are they used in GRUs and LSTMs? How can this be applied? 
- How does Word2Vec differ from GloVe?
- How does Negative Sampling work and how does it impact CBOW?
- What is the difference between CBOW and Skip-Gram? How does this relate to Word2Vec? 







