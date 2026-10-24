# Grokking Deep Learning

Companion notebooks for **[Grokking Deep Learning](https://www.manning.com/books/grokking-deep-learning)** by Andrew W. Trask (Manning).

The book builds neural networks from scratch using Python and NumPy. These notebooks follow the book chapter by chapter, summarizing key concepts, reproducing code examples where applicable, and adding visualizations and small experiments to help make the concepts easier to understand.

> This is a personal study repository, not a replacement for the book. Read the book alongside these notebooks and use the examples to check your understanding and experiment with the code.

## What Each Notebook Covers

### Part 1: Foundations

- **Chapter 1: Introduction.** Introduces deep learning, explains why it is worth learning, describes the book's learning approach, and covers the basic requirements for getting started. Includes an environment check cell.
- **Chapter 2: Fundamental Concepts.** Covers machine learning fundamentals, supervised and unsupervised learning, and parametric and nonparametric learning. Since the book contains no code in this chapter, the hands-on demonstrations are additional examples.

### Part 2: Building and Training Your First Networks

- **Chapter 3: Making Predictions.** Introduces forward propagation with single and multiple inputs and outputs, stacked networks, and the intuition behind the dot product. Covers both pure Python and NumPy implementations.
- **Chapter 4: Gradient Descent.** Explains the learning process through prediction, error comparison, and weight updates. Covers hot and cold learning, `weight_delta`, divergence, and the role of the learning rate `alpha`.
- **Chapter 5: Learning Multiple Weights.** Explores gradient descent with multiple inputs and outputs, weight updates, and the relationship between weights and learned patterns. Includes demonstrations using the 8×8 digits dataset from scikit-learn.
- **Chapter 6: First Deep Network.** Introduces the streetlight problem, stochastic and batch gradient descent, correlation, overfitting, backpropagation, and the importance of ReLU. Concludes with a manually implemented three-layer neural network.
- **Chapter 7: Visualization.** Develops mental models for understanding neural networks through vectors, matrices, correlation, and mathematical notation. Explains how multiple layers can be represented using matrix operations.

### Part 3: Making Networks Work on Real Data

- **Chapter 8: Regularization and Batching.** Covers overfitting, early stopping, dropout, and mini-batch gradient descent. Introduces techniques for improving generalization and training efficiency.
- **Chapter 9: Activation Functions.** Explains the role of activation functions and their mathematical properties. Covers sigmoid, tanh, and softmax, including their use in forward and backward propagation.
- **Chapter 10: Convolutional Neural Networks.** Introduces convolutional neural networks (CNNs), weight sharing, and convolution kernels. Includes NumPy-based implementations and experiments with the MNIST handwritten-digit dataset.

### Part 4: Understanding Language with Neural Networks

- **Chapter 11: Neural Networks That Understand Language.** Introduces natural language processing, sentiment analysis, bag-of-words representations, word embeddings, and vector analogies. Explores how neural networks represent words and learn relationships between them.
- **Chapter 12: Neural Networks That Write Like Shakespeare.** Introduces recurrent neural networks (RNNs), averaged word vectors, sequential data, and variable-length inputs. Explains how neural networks process sequences and learn patterns in text.

### Part 5: Building Deep Learning Frameworks and Improving Sequence Models

- **Chapter 13: Introducing Automatic Optimization.** Explores how to build a deep learning framework from scratch. Covers tensors, automatic differentiation (autograd), gradient calculations, layers, loss functions, and recurrent layers.
- **Chapter 14: Learning to Write Like Shakespeare.** Covers character-level language modeling, truncated backpropagation through time (BPTT), vanishing and exploding gradients, and Long Short-Term Memory (LSTM) networks. Explains how LSTMs help neural networks learn dependencies across longer sequences.

### Part 6: Applying Deep Learning to Unseen Data

- **Chapter 15: Deep Learning on Unseen Data.** Explores privacy-aware machine learning, federated learning, secure aggregation, and homomorphic encryption. Discusses approaches to training models on distributed data while helping protect sensitive information.

## Conventions Used in the Notebooks

- **Reproduced code** follows the book's examples where applicable.
- Additional visualizations, experiments, and sanity checks are identified as personal demonstrations or *Hands-on* sections.
- Each notebook is intended to be run from top to bottom because later cells may reuse variables defined earlier.
- The book encourages readers to re-type code from memory before moving on. The *Memorizing* and *Memorization Challenge* sections support this practice.
- Chapter summaries emphasize the main concepts and learning points of each chapter.

## Requirements

| Package | Used For |
|---|---|
| `numpy` | Numerical operations and neural network implementations |
| `matplotlib` | Plots, visualizations, and network diagrams |
| `scikit-learn` | Chapter 5 demonstrations using the 8×8 digits dataset |
| `keras` *(optional)* | Loading the MNIST dataset in Chapters 8–10 |

Python 3.10 or later is recommended. The original notebooks were reported to have been tested with Python 3.12; compatibility may vary depending on package versions.

Not every package is required for every chapter. Install only the dependencies needed for the notebook you want to run.

## About the MNIST Dataset

Chapters 8–10 use the MNIST handwritten-digit dataset.

The original notebooks attempt to load MNIST through `keras.datasets.mnist`. If Keras is unavailable, some implementations may use an alternative dataset source. An internet connection may be required when the dataset has not already been downloaded.

## Expected Runtime

Runtime depends on the computer, Python environment, package versions, and whether the dataset has already been downloaded.

- **Chapters 1–7:** Expected to run in seconds for the original lightweight examples.
- **Chapter 8:** May take several minutes because it trains neural networks on MNIST.
- **Chapter 10:** May take several minutes depending on the CNN implementation and training configuration.
- **Chapters 9 and 11–15:** Runtime varies according to the specific examples, computations, and implementations in each notebook.

These are approximate expectations rather than guaranteed execution times.

## Repository Structure

```text
GrokkingDeepLearning/
├── Chapter1_Introduction.ipynb
├── Chapter2_Fundamental-Concepts.ipynb
├── Chapter3_Making-Predictions.ipynb
├── Chapter4_Gradient-Descent.ipynb
├── Chapter5_Learning-Multiple-Weights.ipynb
├── Chapter6_First-Deep-Network.ipynb
├── Chapter7_Visualization.ipynb
├── Chapter8_Regularization-and-Batching.ipynb
├── Chapter9_Activation-Functions.ipynb
├── Chapter10_Convolutional-Neural-Networks.ipynb
├── Chapter11_Summary.ipynb
├── Chapter12_Summary.ipynb
├── Chapter13_Summary.ipynb
├── Chapter14_Summary.ipynb
├── Chapter15_Summary.ipynb
└── README.md
```

*Note: The filenames in this structure should match the actual notebook filenames in the repository.*

## Learning Objectives

By working through these notebooks, readers can:

- Understand the fundamental concepts behind neural networks and deep learning.
- Implement basic neural networks using Python and NumPy.
- Understand forward propagation, gradient descent, and backpropagation.
- Explore techniques for improving training and generalization.
- Learn the basic principles of CNNs, RNNs, and LSTMs.
- Understand how neural networks can process language and sequential data.
- Explore automatic differentiation and the components of a deep learning framework.
- Become familiar with privacy-preserving approaches to machine learning.

## Reference

Trask, Andrew W. *Grokking Deep Learning*. Manning Publications.

[Official book page](https://www.manning.com/books/grokking-deep-learning)

---

**Disclaimer:** This repository is intended for educational and personal study purposes. It is an independent learning companion to the book and is not an official Manning Publications repository.

Author: Dhea Kusuma Wardhani
NIM: 101032330059
