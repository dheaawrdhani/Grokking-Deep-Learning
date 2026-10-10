Grokking Deep Learning

Code reproduction and theory notes for Grokking Deep Learning by Andrew W. Trask (Manning). This repository is my submission for Task 2 (Enrichment for Deep Learning Classes): Code Reproduction + Theoretical Deep-Dive.

Every neural network here is built from scratch with plain Python and NumPy (no TensorFlow/PyTorch), following the book chapter by chapter. Each notebook mixes three things:

a summary of the chapter's theory, one section per sub-chapter of the book,
the book's code, rebuilt and executed in Google Colab (with outputs saved), and
extra visualisations and small experiments (network diagrams, error curves, alpha sweeps) that I added to make the ideas easier to see.

Chapter summaries
Chapter 1: Introducing Deep Learning

A motivational chapter. It argues that deep learning is worth learning because it automates intelligence incrementally, can reshape skilled work, and is genuinely creative and fun. It also explains the book's teaching approach: only high-school math, an analogy for every formula, a "science under the frameworks" focus, and a project-first structure. Prerequisites are Python basics, Jupyter (here, Colab) and NumPy. Notebook extras: environment check, comparison table of the book's selling points, self-check questions.

Chapter 2: Fundamental Concepts

Places deep learning inside machine learning inside AI, then classifies every ML algorithm along two independent axes: supervised vs. unsupervised (learning a mapping between datasets vs. clustering data) and parametric vs. nonparametric (fixed number of "knobs" tuned by trial and error vs. parameters that grow with the data, typically counts). Deep learning is parametric. The chapter also lays out the three-step supervised parametric loop: predict, compare, learn. Notebook extras: a nested-circle diagram, a one-knob Monday → Tuesday learner, k-means clustering, group-membership probabilities, and a counting model whose size grows with the data.

Chapter 3: Forward Propagation (Making Predictions)

Builds the predict step in increasing complexity: one input/one weight, multiple inputs (weighted sum = dot product), multiple outputs, multiple inputs and outputs (vector–matrix multiplication), and stacked networks with a hidden layer. Along the way: vectors, matrices, elementwise operations, the dot product as a similarity measure (AND / NOT intuition), and a NumPy primer centred on shapes and the dot rule (a,b)·(b,c) → (a,c). Notebook extras: a reusable draw_net function that draws every architecture with its weights, the vector-toolkit challenge, and shape exercises.

Chapter 4: Introduction to Gradient Descent

Builds the compare and learn steps. Error is measured with squared error (positive, emphasises large misses). Hot and cold learning finds the direction by wiggling the weight but is slow and has an arbitrary step. Gradient descent gets direction and amount from weight_delta = input * (pred - goal_pred), which also handles stopping, negative reversal and scaling. The derivative is explained as the sensitivity (slope) between weight and error; large inputs cause divergence, which alpha cures by shrinking each update. Notebook extras: the error "bowl" with its tangent, a weight-path plot, over-correction visualisation, an alpha sweep (0.001 to 0.6 and a negative alpha), and a hot-and-cold vs. gradient-descent cost comparison (about 3300 predictions vs. 22).
