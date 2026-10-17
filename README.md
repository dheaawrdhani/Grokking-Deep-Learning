# Grokking Deep Learning

Companion notebooks for **[Grokking Deep Learning](https://www.manning.com/books/grokking-deep-learning)** by Andrew W. Trask (Manning). The book builds neural networks from scratch with nothing but Python and NumPy. These notebooks follow it chapter by chapter: each one summarizes the chapter, reproduces its code, and adds plots and small experiments so every idea can be *seen* running.

> This is a personal study repository, not a replacement for the book. Read the book first; use the notebooks to check your understanding and to run the code.


## What each notebook covers

**Part 1: Foundations (no or little code in the book)**
- **Chapter 1: Introduction.** Why deep learning is worth learning, how the book teaches it, and what you need to start. Includes an environment check cell.
- **Chapter 2: Fundamental Concepts.** Machine learning, supervised vs. unsupervised, parametric vs. nonparametric learning. The book has no code here, so the demos are my own and are labelled *Hands-on*.

**Part 2: Building and training your first networks**
- **Chapter 3: Making Predictions.** Forward propagation with one and many inputs and outputs, stacked networks, the intuition behind the dot product; pure Python first, then NumPy, with diagrams drawn in Matplotlib.
- **Chapter 4: Gradient Descent.** The *predict → compare → learn* loop: error, hot and cold learning, `weight_delta`, divergence and the role of `alpha`.
- **Chapter 5: Learning Multiple Weights.** Gradient descent with multiple inputs and outputs, freezing a weight, and visualizing what weights learn (uses scikit-learn's 8×8 digits so it runs offline).
- **Chapter 6: First Deep Network.** The streetlight problem, stochastic/batch/full gradient descent, correlation and overfitting, backpropagation, and why relu matters. Ends with a three-layer network built by hand.
- **Chapter 7: Visualization.** Mental models and notation: the correlation summarization, networks as vectors and matrices, `l2 = relu(l0 W0) W1`.

**Part 3: Making networks work on real data (MNIST)**
- **Chapter 8: Regularization and Batching.** Overfitting, early stopping, dropout, mini-batch gradient descent.
- **Chapter 9: Activation Functions.** The constraints a good activation must satisfy, sigmoid/tanh/softmax, installing an activation in the forward and backward passes, and the upgraded MNIST network.
- **Chapter 10: Convolutional Neural Networks.** Reusing weights, what a convolution kernel does on real digits, the book's NumPy implementation trained on MNIST. Includes a note on a sign inconsistency in the book's listing.

## Conventions used in the notebooks

- **Reproduced code** follows the book's listings. Where I add something of my own (plots, extra experiments, sanity checks) it is marked as *my demo* or *Hands-on*.
- Each notebook is meant to be run **top to bottom**; later cells reuse variables defined earlier.
- The book's advice is to **re-type the code from memory** before moving on. The *Memorizing* / *Memorization challenge* sections are there for that purpose.


### Requirements
| Package | Used for |
|---------|----------|
| `numpy` | everything; the only numerical library the book uses |
| `matplotlib` | plots and network diagrams |
| `scikit-learn` | Chapter 5 only (bundled 8×8 digits dataset) |
| `keras` *(optional)* | loading MNIST in Chapters 8–10 |

Python 3.10+ is recommended (notebooks were last run on 3.12).

### About the MNIST data (Chapters 8–10)
The notebooks first try `keras.datasets.mnist`, as the book does. If Keras isn't installed, they fall back to downloading the same dataset from a public GitHub mirror (`mnist.pkl.gz`, saved next to the notebook), so an internet connection is the only requirement.

### Expected runtime
Chapters 1–7 run in seconds. Chapter 8 takes roughly **3–5 minutes** and Chapter 10 about **5 minutes**, because they train several networks on MNIST.

## Repository structure

```
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
└── README.md
```

## Prerequisites

High-school math and basic Python (variables, lists, loops, functions). The book explains the linear algebra, calculus and machine learning it needs as it goes.

## Credits and license

All concepts, listings and the book's structure belong to **Andrew W. Trask** and **Manning Publications**. Please buy the book and consult it and its [official code repository](https://github.com/iamtrask/Grokking-Deep-Learning) for authoritative content and licensing. The summaries, extra plots and experiments in this repository are my own study notes.
