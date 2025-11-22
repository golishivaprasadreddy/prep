### 32. What is the difference between accuracy and precision?  
Accuracy measures how often the model’s predictions are correct overall, while precision measures how many predicted positives are actually true positives.

### 33. How can learning curves indicate if more data will improve performance?  
If training and validation curves are close but both have high error, more data is unlikely to help. If there is a large gap (validation worse), adding data may reduce overfitting and improve performance.

### 34. What is the purpose of checking gradients?  
Gradient checking verifies that backpropagation is implemented correctly by comparing analytical gradients with numerical approximations, helping detect errors in training logic.

### 35. How does distributed training enable scaling of deep models?  
Distributed training divides computation across multiple GPUs or machines, enabling faster training and handling larger models and datasets than a single device can support.

### 36. What type of neural network is most commonly used in computer vision?  
Convolutional Neural Networks (CNNs) are most commonly used due to their ability to capture spatial patterns and reduce parameters through weight sharing.

### 37. How can reinforcement learning extend deep learning beyond supervised learning?  
Reinforcement learning trains models through interaction with an environment using rewards instead of labeled data, enabling learning of sequential decision-making tasks.

### 38. What input representation is typically used in speech recognition?  
Speech recognition systems commonly use **spectrograms** or **Mel-frequency cepstral coefficients (MFCCs)** as input representations derived from audio signals.

### 39. Why are convolutional layers well-suited for image processing?  
Convolutional layers exploit local spatial structure through small receptive fields and shared weights, enabling them to efficiently detect patterns like edges, textures, and shapes in images.
