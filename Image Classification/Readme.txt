Title:
Few-Shot Learning for Image Classification

Project Description:
This code implements a Few-Shot Image Classification system using a ResNet-18 model pre-trained on ImageNet. Few-shot learning is achieved by limiting the number of samples per class (5 samples in this case) for training. The project focuses on fine-tuning a pre-trained model for classification tasks with a small dataset and validating its performance.

Approach:
Data Preparation:

Dataset Loading: The dataset is loaded using torchvision.datasets.ImageFolder, which expects a directory structure where each subdirectory represents a class.
Few-Shot Sampling: Each class is limited to a specified number of samples (num_shots = 5) by manually selecting indices.
Splitting: The few-shot dataset is divided into training and validation subsets using train_test_split.
Data Augmentation:

Images are resized to 224x224 and normalized using ImageNet mean and standard deviation for compatibility with the pre-trained ResNet-18.
Model Setup:

The ResNet-18 model is modified by replacing the fully connected layer (fc) with a new layer to match the number of target classes (num_classes = 5).
Pre-trained weights are retained to leverage transfer learning.
Training:

Loss Function: CrossEntropyLoss is used for multi-class classification.
Optimizer: Adam optimizer is configured with a learning rate of 0.001.
Training Loop:
The model is trained for num_epochs epochs, updating weights using backpropagation.
Metrics such as training loss and accuracy are calculated.
Validation:

The model's performance is evaluated on the validation set after each epoch.
Metrics such as validation loss and accuracy are computed.
Metrics:
Training Metrics:

Loss: Tracks the CrossEntropyLoss over the training set.
Accuracy: Measures the proportion of correctly classified samples during training.
Validation Metrics:

Loss: Computes CrossEntropyLoss over the validation set to monitor overfitting.
Accuracy: Measures the proportion of correctly classified samples in the validation set