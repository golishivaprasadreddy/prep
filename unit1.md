
📘 Set 4 – Questions & Answers

---

**1. Compare shallow versus deep architectures in terms of representational power, training complexity, and generalization ability.**

* **Representational Power:**

  * *Shallow Architectures:* Limited to learning simple patterns, struggle with capturing hierarchical or complex structures.
  * *Deep Architectures:* Can represent highly complex functions by stacking multiple layers, learning hierarchical features (low-level → mid-level → high-level).

* **Training Complexity:**

  * *Shallow Models:* Easier to train with fewer parameters, but may underfit complex tasks.
  * *Deep Models:* Training is harder due to vanishing/exploding gradients, requires large datasets, careful initialization, and optimizers.

* **Generalization Ability:**

  * *Shallow Models:* Risk of underfitting, but often more stable with smaller datasets.
  * *Deep Models:* If trained well, generalize better by capturing intricate patterns, but prone to overfitting without regularization.

**Conclusion:** Deep architectures provide greater representational power and generalization when supported by enough data and regularization, while shallow models are simpler but limited in capability.

---

**2. Analyze the fundamental differences in how supervised and unsupervised learning algorithms approach the problem of classification and clustering.**

* **Supervised Learning (Classification):**

  * Uses labeled data (input + target).
  * Learns a direct mapping from features to labels.
  * Objective: Minimize classification error.
  * Example: Logistic Regression, CNNs, Random Forest.

* **Unsupervised Learning (Clustering):**

  * Works with unlabeled data.
  * Groups similar samples based on inherent structure or distance metrics.
  * Objective: Find hidden patterns or structures.
  * Example: K-Means, DBSCAN, Autoencoders.

* **Key Difference:**

  * Classification assigns predefined labels, clustering discovers natural groupings without prior knowledge.

**Conclusion:** Supervised learning requires ground-truth labels to predict outcomes, while unsupervised learning extracts structure from raw data.

---

**3. Apply L1 and L2 norm penalties to a simple linear regression model. How would the coefficients change under each penalty?**

* **L1 Norm (Lasso Regression):**

  * Adds penalty proportional to |weights|.
  * Encourages sparsity → some coefficients become exactly zero.
  * Useful for feature selection.

* **L2 Norm (Ridge Regression):**

  * Adds penalty proportional to weights².
  * Shrinks coefficients but rarely to zero.
  * Useful for reducing multicollinearity and improving stability.

**Coefficient Behavior:**

* L1 → Sparse solution (feature elimination).
* L2 → Small but nonzero coefficients (feature shrinkage).

**Conclusion:** L1 leads to sparsity and feature selection, while L2 promotes smoother weight distribution and prevents large coefficients.

---

**4. Apply regularization techniques to prevent overfitting in a model trained on a small dataset. Which method would you choose and why?**

* **Options:**

  * L1/L2 Regularization (penalize large weights).
  * Dropout (randomly deactivate neurons during training).
  * Data Augmentation (synthetically increase dataset size).
  * Early Stopping (halt training before overfitting).

* **Best Choice for Small Dataset:**

  * *Data Augmentation* → directly increases data diversity without collecting more samples.
  * Combine with *L2 regularization* → avoids large unstable weights.

**Conclusion:** For small datasets, data augmentation is most effective, supported by L2 regularization and early stopping to prevent overfitting.

---

**5. Analyze how convolutional architectures can be adapted to handle structured outputs such as segmentation maps instead of scalar predictions.**

* **Scalar Predictions (e.g., classification):**

  * CNNs compress spatial information through pooling + fully connected layers.
  * Output is a single class label or probability vector.

* **Structured Outputs (e.g., segmentation maps):**

  * Need per-pixel predictions instead of a single label.
  * Adaptations:

    * *Fully Convolutional Networks (FCNs):* Replace fully connected layers with convolution layers to maintain spatial dimensions.
    * *Upsampling/Deconvolution:* Use transposed convolutions or interpolation to recover image resolution.
    * *Skip Connections:* Combine low-level spatial details with high-level semantic features (e.g., U-Net).

**Conclusion:** Convolutional architectures are adapted with FCNs, upsampling, and skip connections to produce structured outputs like segmentation maps.

---

**6. Analyze how convolution differs from fully connected layers in terms of parameter efficiency and inductive bias.**

* **Fully Connected Layers (FC):**

  * Each neuron connects to every input.
  * Parameters = Input size × Output size.
  * No spatial locality assumption → treats all pixels equally.
  * Computationally expensive, high risk of overfitting.

* **Convolutional Layers (Conv):**

  * Uses local receptive fields with shared filters.
  * Parameters = Kernel size × Channels (much fewer than FC).
  * Exploits spatial locality → nearby pixels are correlated.
  * Captures translation invariance (feature detection independent of position).

* **Inductive Bias:**

  * FC Layers: No prior assumptions, flexible mappings.
  * Conv Layers: Assumes local patterns matter, suitable for vision tasks.

**Conclusion:** Convolutional layers are parameter-efficient and leverage spatial inductive biases, while fully connected layers are more flexible but prone to overfitting and inefficiency for image data.
