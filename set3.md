
📘 Set 3– Questions & Answers

**1. Analyze why traditional machine learning algorithms struggle with tasks like image recognition and how deep learning addresses these challenges.**

**Traditional ML Struggles:**

* **Feature Engineering Dependency:** Classical ML (e.g., SVM, logistic regression, decision trees) relies on hand-crafted features (edges, textures, shapes). Designing these features manually is time-consuming and often incomplete.
* **High Dimensionality:** Images are large matrices of pixels (e.g., 224×224×3 = \~150k features). Traditional ML cannot efficiently handle such high-dimensional raw data without dimensionality reduction.
* **Scalability Issues:** Training becomes inefficient as dataset size and dimensionality grow, leading to poor generalization.
* **Limited Representation Power:** Shallow models cannot automatically capture hierarchical structures (edges → patterns → objects).

**How Deep Learning Solves This:**

* **Automatic Feature Extraction:** CNNs automatically learn low-level (edges), mid-level (textures), and high-level (objects) features directly from raw pixels.
* **Parameter Sharing:** Convolutional layers reuse filters across the image, drastically reducing parameters compared to fully connected layers.
* **Scalability with Data:** Deep networks improve with more data, while traditional ML often plateaus.
* **Transfer Learning:** Pretrained models (e.g., ResNet, VGG) can be fine-tuned for new tasks, something traditional ML cannot leverage easily.

**Conclusion:** Deep learning bypasses manual feature engineering and effectively handles high-dimensional, large-scale image data, making it ideal for recognition tasks.

---

**2. Provide an example of a situation where improper tuning leads to poor performance.**

**Example – Neural Network Training:**

* **Very High Learning Rate:**

  * Causes weight updates to overshoot the optimal point.
  * Loss fluctuates or even diverges.
  * Training never converges → poor accuracy.

* **Very Low Learning Rate:**

  * Training is extremely slow.
  * Model may get stuck in local minima.
  * Final accuracy is suboptimal.

* **Improper Regularization (e.g., Dropout too high):**

  * Too many neurons deactivated → underfitting.
  * Model fails to capture necessary patterns.

* **Batch Size Misconfiguration:**

  * Too small → noisy gradients.
  * Too large → poor generalization.

**Conclusion:** Improper tuning of hyperparameters (learning rate, dropout, batch size, etc.) can either prevent convergence or cause under/overfitting, leading to poor model performance.

---

**3. In what way adversarial training is used for regularization in deep learning?**

**What are Adversarial Examples?**

* Small, imperceptible perturbations added to input images that fool the model into making wrong predictions (e.g., classifying a cat as a dog).

**Adversarial Training:**

* Augment the dataset with adversarially perturbed inputs.
* Train the model to correctly classify both clean and adversarial inputs.
* Forces the network to learn more robust representations rather than memorizing data.

**Benefits as Regularization:**

* **Robustness:** Makes model resistant to adversarial attacks.
* **Generalization:** Prevents overfitting by exposing the model to harder examples.
* **Improved Feature Learning:** Learns smoother decision boundaries that generalize better.

**Conclusion:** Adversarial training is a form of data augmentation + regularization that strengthens robustness, reduces overfitting, and improves generalization in deep learning.

---

**4. How batch normalization can be used in optimization?**

**Problem in Optimization:**

* During training, input distributions to each layer shift (called internal covariate shift).
* Leads to unstable gradients and slower convergence.

**Batch Normalization (BN):**

* Normalizes activations of each layer for every mini-batch.
* Keeps mean ≈ 0 and variance ≈ 1.
* Introduces learnable parameters (γ, β) to restore scaling and shifting when needed.

**Role in Optimization:**

* **Stabilizes Training:** Reduces internal covariate shift.
* **Enables Higher Learning Rates:** Prevents gradient explosion/vanishing.
* **Regularization Effect:** Adds slight noise due to batch statistics → acts like dropout.
* **Faster Convergence:** Models train in fewer epochs.
* **Better Generalization:** Helps networks achieve higher accuracy.

**Conclusion:** Batch normalization improves optimization by stabilizing gradients, speeding up convergence, and allowing efficient use of higher learning rates.

---

**5. Analyze how convolution differs from fully connected layers in terms of parameter efficiency and inductive bias.**

**Fully Connected Layers (FC):**

* Each neuron connects to every input.
* Parameters = Input size × Output size.
* No spatial locality assumption → treats all pixels equally.
* High risk of overfitting for images due to enormous parameter count.

**Convolutional Layers (Conv):**

* Uses small kernels/filters that slide over the image.
* Parameters = Kernel size × Channels (much fewer than FC).
* Exploits spatial locality → nearby pixels are related.
* **Parameter Sharing:** Same filter applied everywhere.
* Captures translation invariance → detects features regardless of position.

**Inductive Bias:**

* **FC Layers:** No prior assumptions, can learn arbitrary mappings.
* **Conv Layers:** Strong assumption that local patterns matter → well-suited for vision.

**Conclusion:** Convolutional layers are parameter-efficient and encode inductive biases (locality, translation invariance), while fully connected layers are flexible but computationally expensive and prone to overfitting.


📘 Set – Questions & Answers

---

### 6. Compare the effect of max pooling versus average pooling on feature maps. In which scenarios might each pooling strategy lose critical information?

**Max Pooling:**

* Selects the maximum value from a local receptive field (patch).
* Captures the most dominant activation within that region.
* Preserves sharp features like edges, corners, and strong signals.
* **Limitation:** May discard subtle but useful information such as textures or faint patterns.

**Average Pooling:**

* Computes the mean value of the local receptive field.
* Retains smoother, generalized features across the region.
* Useful for preserving background or contextual information.
* **Limitation:** Can weaken strong distinctive signals, such as edges, by averaging them out.

**Comparison & Use Cases:**

* **Max Pooling** is better suited for classification tasks where sharp, discriminative features (like object edges and shapes) are essential.
* **Average Pooling** is beneficial in tasks requiring context preservation, noise reduction, or smooth representation (e.g., image segmentation).

**Conclusion:**
Max pooling highlights strong features but risks losing fine details, while average pooling retains overall information but can dilute distinct signals. The choice depends on whether the task prioritizes sharp feature detection or smooth context preservation.

