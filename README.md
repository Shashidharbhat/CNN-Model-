# CNN-Model
The dataset comprises 90 different animal images. Initially, we'll structure it for one-vs-rest classification, followed by binary classification and then a 5-class classification problem. We'll evaluate each model's performance using classification matrices.
1. Dataset Preparation:
   - Organize the dataset for one-vs-rest classification. Perform binary classification using existing architectures and then restructure for 5-class classification. Use 3-fold cross-validation to assess the model.

2. Model Development:
   - Build a custom CNN model without using existing architectures like ResNet or DenseNet.

3. Training and Evaluation:
   - Train the model on prepared datasets for one-vs-rest and 5-class classification.
   - Generate classification matrices for visualization.
4. Convolutional Layer Visualization:
   - Plot the output of all convolutional layers and discuss the insights on automatically created features.
Feature Extraction: The model used is BasicCnn, which is a deep convolutional neural networks pre-trained on the ImageNet dataset. During training, Cnn model learns to extract hierarchical features from input images. The initial layers capture low-level features like edges and textures, while deeper layers capture high-level semantic features like shapes and object parts. By using this model, we benefit from the features learned during its training.
Dimensionality Reduction: The features extracted from the CustomCnn model typically have a high dimensionality. However, by using them as input to a linear classifier (fully connected layer), we effectively reduce the dimensionality of the feature space while preserving the most discriminative information. This helps in improving the efficiency of training and inference.
Class Discriminative Features: The features extracted from the CustomCnn model are learned in such a way that they are discriminative for distinguishing between different classes. This is crucial for effective classification performance, as the model needs to learn features that are informative for distinguishing between the classes in your dataset.
