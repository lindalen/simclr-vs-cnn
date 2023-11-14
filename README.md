# Self-Supervised Learning with SimCLR on CIFAR-10

## Overview
This project explores the implementation of Self-Supervised Learning (SSL) using the SimCLR framework on the CIFAR-10 dataset. The focus is on comparing the performance of a model trained with SSL followed by a linear classifier, against a basic Convolutional Neural Network (CNN).

## Key Features
- **SSL Implementation:** Utilizes the SimCLR approach for self-supervised learning.
- **Dynamic Data Sampling:** A novel tweak involves using a different subset of data in each epoch during training, enhancing the diversity of training samples.
- **Performance:** The SSL plus linear classifier model achieved an accuracy of 88.86%.
- **Comparison Model:** A basic CNN model was used for comparison, achieving an 81% accuracy, indicating potential areas for improvement.

## Implementation Details
- **Self-Supervised Learning (SSL):** The SimCLR model was pre-trained on CIFAR-10 using self-supervised techniques. 
- **Batch Size Consideration:** Due to hardware limitations, the batch size used for SSL pre-training was smaller than recommended in the original SimCLR paper.
- **Linear Classifier:** Post SSL pre-training, a linear classifier was trained on top of the frozen representations.

## Results and Discussion
- The SSL with a linear classifier model outperformed the basic CNN model.
- A unique approach of changing subsets each epoch was employed, which could have implications on model generalization and robustness.
- The project didn't reach the accuracy reported in the original SimCLR paper, potentially due to differences in batch size during SSL pre-training.

## If I had more time and a stronger GPU:
- **Model Scaling:** Experiment with larger models and batch sizes as hardware resources permit. (resnet50 for example)
- **CNN Enhancement:** Refine the CNN architecture and training approach to improve its performance.
- **Further Experiments:** Explore the impact of different data sampling strategies on model performance.

## References
- Original Code Repository: [SimCLR-CIFAR10](https://github.com/p3i0t/SimCLR-CIFAR10/tree/master)
