📘 Set 1 – Questions & Answers
1. Given two learning curves, identify which model is overfitting and which is underfitting. Justify your reasoning.

Overfitting:

Training accuracy is very high, but validation accuracy is much lower.

A wide gap exists between the two curves after several epochs.

The model has learned training data very well, even memorizing noise.

It fails to generalize to unseen/validation data.

Example: Very deep neural network with no regularization.

Underfitting:

Both training and validation accuracies are low.

The two curves stay close to each other.

The model is too simple or not trained enough.

It cannot capture patterns in the data.

Example: Linear model used for a highly nonlinear dataset.

Conclusion:

Large gap → Overfitting

Both low & close → Underfitting

Ideal model → high training & validation accuracy with a small gap

2. Analyze how hyperparameter tuning with validation sets can help balance bias and variance.

High Bias (Underfitting):

Model is too simple, cannot capture patterns.

Example: very shallow tree, too few layers.

Solution: increase model capacity (e.g., more layers, higher depth).

High Variance (Overfitting):

Model fits training data too well but fails on validation data.

Example: very deep tree, very high learning rate.

Solution: add regularization, reduce complexity, adjust learning rate.

Role of Validation Set:

Provides unbiased feedback on unseen data.

Helps select best hyperparameters by testing different settings.

Achieves a balance between training and generalization.

Conclusion:
Hyperparameter tuning with validation sets prevents both underfitting and overfitting, ensuring better generalization.

3. How optimization is used to train the deep models.

Optimization is the process of adjusting model parameters (weights and biases) so that the model performs better on a given task by minimizing the loss function.

Initialization: Deep models start with random weights.

Forward Pass: Input data is passed through the network to calculate predictions.

Loss Calculation: The error (loss) is computed by comparing predictions with actual labels.

Backpropagation: Gradients of the loss with respect to model weights are calculated using the chain rule.

Optimization Algorithms:

Gradient Descent (GD): Updates weights by moving in the opposite direction of the gradient.

Stochastic Gradient Descent (SGD): Updates using small batches for efficiency.

Adam, RMSProp: Advanced optimizers that adapt learning rates for faster convergence.

Iteration: This process repeats over many epochs until the model converges to a good solution.

Conclusion:
Optimization is the core process that allows deep models to learn from data, minimize errors, and improve accuracy over time.

4. How is noise used as a regularizer? Justify.

Noise is intentionally added during training to reduce overfitting and improve the model’s ability to generalize to new data.

Why Needed?

Deep models may memorize training data (overfitting).

Noise forces the model to focus on general patterns rather than memorizing.

Types of Noise:

Input Noise: Small random variations added to input data (e.g., adding Gaussian noise to images).

Weight Noise: Random noise added to weights during training, preventing reliance on exact values.

Dropout: A popular technique where random neurons are "dropped" (deactivated) during training, forcing the network to learn multiple paths for prediction.

Benefits:

Improves robustness to unseen/noisy real-world data.

Makes the model more stable and less sensitive to small input variations.

Acts like an ensemble of multiple smaller models.

Conclusion:
Noise is a powerful regularization method that prevents overfitting, improves generalization, and ensures the model is robust and reliable in practice.

5. Analyze the convolution operation with an example of 2-D convolution.

Convolution is a mathematical operation widely used in deep learning for image and signal processing. It extracts features by sliding a filter (kernel) over the input data.

Process:

A kernel (e.g., 3×3) slides across the image (e.g., 5×5).

For each position, element-wise multiplication is done between the kernel and the image patch.

The results are summed to produce one value in the feature map.

This process repeats as the kernel moves, creating the full output map.

Example:

Input Image: 5×5 matrix

Kernel: 3×3 matrix (e.g., edge detection filter)

Output: 3×3 feature map

If the kernel detects horizontal edges, the output highlights those regions of the image.

Advantages:

Captures local patterns (edges, textures, corners).

Reduces dimensionality while keeping important features.

Can be stacked to capture higher-level features (shapes, objects).

Conclusion:
2-D convolution transforms raw data into meaningful feature maps, making it the backbone of computer vision tasks like image classification, detection, and recognition.

6. Compare standard convolution, dilated convolution, and depthwise separable convolution in terms of computational cost and representational capacity.

Standard Convolution:

Each filter operates on all input channels.

High computational cost.

Strong representational capacity (captures rich features).

Dilated Convolution:

Inserts gaps (dilations) inside kernel.

Expands receptive field without more parameters.

Moderate cost, good for long-range dependencies.

Depthwise Separable Convolution:

Breaks convolution into depthwise (per channel) + pointwise (1×1).

Much lower computational cost.

Slightly reduced capacity but efficient (e.g., MobileNet).

Conclusion:

Standard → Best accuracy, highest cost.

Dilated → Larger receptive field at low cost.

Depthwise separable → Very efficient, suitable for lightweight models.
