### 9. What does L2 regularization penalize?  
L2 regularization penalizes the **sum of squared weights** in a model. It discourages large parameter values, helping reduce overfitting by smoothing the model.

### 10. Why does L1 regularization promote sparsity in parameters?  
L1 regularization penalizes the **absolute values of weights**, which pushes many weights exactly to zero. This creates sparse models with fewer active parameters.

### 11. What is the main purpose of regularization?  
The main purpose of regularization is to **reduce overfitting** by constraining the model’s complexity. It helps the model generalize better to unseen data.

### 12. How does noise injection during training improve generalization?  
Injecting noise (e.g., in inputs or weights) forces the model to learn **robust features** instead of memorizing training data. This reduces overfitting and improves generalization.

### 13. What is the stopping criterion in early stopping?  
Early stopping halts training when the **validation loss stops improving** for a set number of epochs, preventing the model from overfitting.

### 14. Why are sparse representations efficient in neural networks?  
Sparse representations use fewer active neurons, which reduces computation and improves memory efficiency. They also help models focus on the most important features.

### 15. What does tangent distance measure?  
Tangent distance measures the **similarity between images** by considering small transformations such as rotation or translation. It compares images along allowable transformation directions.

### 16. Why do vanishing gradients hinder training of deep networks?  
When gradients become extremely small during backpropagation, early layers receive almost no updates. This slows or stops learning in deep networks, making training ineffective.
