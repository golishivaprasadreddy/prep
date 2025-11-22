### 1. What is the role of a learning algorithm in machine learning?  
A learning algorithm updates the model’s parameters based on training data so the model can generalize to unseen samples. It automates the process of finding patterns and minimizing error.

### 2. Why do we use a validation set instead of only training and test sets?  
A validation set helps tune hyperparameters and select the best model without overfitting to the test set. It ensures that the final test accuracy remains an unbiased measure of true performance.

### 3. How is MLE related to fitting parameters in a probabilistic model?  
Maximum Likelihood Estimation chooses parameter values that maximize the probability (likelihood) of the observed data. It provides a systematic way to estimate parameters in probabilistic models.

### 4. What does bias represent in a model?  
Bias indicates the error due to overly simple assumptions in the model. High bias means the model underfits and fails to capture the actual patterns in the data.

### 5. Give one challenge that motivated deep learning.  
Traditional ML required manual feature engineering, which was difficult for complex data like images and speech. Deep learning overcame this by automatically learning features.

### 6. How does Bayes’ theorem update probabilities?  
Bayes’ theorem updates prior probabilities using new evidence to produce a posterior probability:  
P(H|D) = (P(D|H) × P(H)) / P(D).  
It combines prior belief with observed data.

### 7. What determines the depth of a neural network?  
The depth is determined by the number of hidden layers between the input and output. More hidden layers mean a deeper and more expressive neural network.

### 8. Why do hidden units allow neural networks to model complex functions?  
Hidden units apply nonlinear activation functions, enabling the network to learn complex, nonlinear relationships and represent hierarchical patterns in data.
