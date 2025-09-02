**📘 Set 2 – Expanded Questions & Answers**

**1. Compare and contrast Maximum Likelihood Estimation (MLE) and Bayesian methods in terms of assumptions, flexibility, and use cases.**

**Maximum Likelihood Estimation (MLE):**

* **Assumptions:** Assumes that the best model parameters are those that maximize the likelihood of the observed data. It does not incorporate prior beliefs.
* **Flexibility:** Less flexible since it relies only on the given dataset. It can be sensitive to small sample sizes and noisy data.
* **Use Cases:** Commonly used when data is abundant, prior information is unavailable, or computation needs to be efficient. Examples: logistic regression, linear regression.

**Bayesian Methods:**

* **Assumptions:** Combine prior beliefs with observed data using Bayes’ theorem. Priors can encode domain knowledge.
* **Flexibility:** More flexible, as they naturally account for uncertainty by producing probability distributions over parameters instead of point estimates.
* **Use Cases:** Useful when data is limited, uncertainty estimation is important, or prior knowledge is valuable. Examples: Bayesian networks, Bayesian inference in reinforcement learning.

**Conclusion:**

* **MLE →** Simpler, efficient, suitable for large datasets but less robust with small/noisy data.
* **Bayesian →** More flexible, accounts for uncertainty, suitable when prior knowledge or uncertainty quantification is critical.

---

**3. In how many ways dataset augmentation are used in regularization of Deep Learning?**

**Definition:** Dataset augmentation increases the diversity of training data by applying transformations, making models more robust and reducing overfitting.

**Common Ways:**

* **Image Transformations:** Flipping, rotation, scaling, cropping, shifting.
* **Noise Addition:** Adding Gaussian noise, salt-and-pepper noise to inputs.
* **Color/Lighting Adjustments:** Varying brightness, contrast, hue, saturation.
* **Mixup & CutMix:** Combining two images (and labels) or replacing patches of one with another.
* **Generative Approaches:** Using GANs or VAEs to synthesize realistic new samples.
* **Text Augmentation (for NLP):** Synonym replacement, back translation, random word insertion/deletion.

**Benefits:**

* Encourages invariance to transformations.
* Reduces overfitting by exposing the model to more variations.
* Improves generalization to unseen data.

**Conclusion:** Dataset augmentation provides multiple strategies across domains (vision, text, audio), acting as a powerful form of regularization.

---

**5. Analyze how convolution differs from fully connected layers in terms of parameter efficiency and inductive bias.**

**Fully Connected (Dense) Layers:**

* **Parameter Efficiency:** Every neuron connects to every input feature → very high number of parameters.
* **Inductive Bias:** No built-in assumption about input structure. Learns general mappings but struggles with structured data like images.
* **Example:** For a 256×256 image with 3 channels, a fully connected layer with 1,000 neurons would need millions of parameters.

**Convolutional Layers:**

* **Parameter Efficiency:** Filters (kernels) are shared across the input. A 3×3 filter has only 9 parameters (per channel), regardless of image size.
* **Inductive Bias:** Enforces spatial locality (neighboring pixels are related) and translation invariance (patterns matter irrespective of location).
* **Example:** A few 3×3 filters can extract edges, textures, and patterns with far fewer parameters than dense layers.

**Conclusion:**

* **Fully Connected →** Very flexible but parameter-heavy, prone to overfitting on structured data.
* **Convolutional →** Efficient, captures spatial hierarchies, strongly suited for vision tasks.

---

**6. Compare standard convolution, dilated convolution, and depthwise separable convolution in terms of computational cost and representational capacity.**

**Standard Convolution:**

* **Process:** Each filter slides over the input and processes all channels.
* **Computational Cost:** High, as every filter processes all input channels.
* **Representational Capacity:** Strong, can capture complex patterns and interactions across channels.
* **Use Cases:** High-performance models like VGG, ResNet.

**Dilated Convolution:**

* **Process:** Introduces gaps (dilations) between filter elements, enlarging receptive field without increasing parameters.
* **Computational Cost:** Similar to standard convolution but captures broader context.
* **Representational Capacity:** Good for modeling long-range dependencies.
* **Use Cases:** Segmentation tasks (e.g., DeepLab), audio/speech modeling.

**Depthwise Separable Convolution:**

* **Process:** Splits convolution into depthwise (per channel) and pointwise (1×1 across channels).
* **Computational Cost:** Much lower compared to standard convolution.
* **Representational Capacity:** Slightly reduced, but sufficient for many tasks.
* **Use Cases:** Mobile and efficient architectures (e.g., MobileNet, EfficientNet).

**Conclusion:**

* **Standard →** High cost, strong accuracy.
* **Dilated →** Efficient way to expand receptive field.
* **Depthwise Separable →** Lightweight, optimal for real-time and mobile applications.
