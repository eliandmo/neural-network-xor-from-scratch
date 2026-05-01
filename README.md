# Training a Neural Network by Hand: The XOR Problem

This repository documents a deep-dive learning activity into the mathematical foundations of Artificial Intelligence. It features a "from scratch" implementation of a feedforward neural network to solve the **XOR (exclusive-OR)** problem, focusing on **Backpropagation** and **Gradient Descent** without the use of high-level ML libraries.

Developed for the course **Fundamentals of AI with Neural Networks and Transformers** at **Universidad del Norte** (Barranquilla, Colombia).

## 🚀 Project Access
- **Live Interactive Report:** [View GitHub Pages Report](https://eliandmo.github.io/neural-network-xor-from-scratch/)
- **Interactive Notebook:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/eliandmo/neural-network-xor-from-scratch/blob/main/xor_final.ipynb)
- **Technical Paper (PDF):** [Download xor_report.pdf](./xor_report.pdf)

## 📋 Executive Summary
The project follows a pedagogical path from manual scalar calculations to vectorized matrix optimizations:
* **Manual Verification:** Step-by-step computation of the 3rd training epoch, yielding $\hat{y}=0.57924$ and $E=0.08852$.
* **Automated Training:** 15-epoch analysis demonstrating monotone loss reduction and the "frozen weight" phenomenon when input $x_1=0$.
* **Sensitivity Analysis:** Comparison between original and alternative initializations, showing a 3.3x improvement in loss reduction when using non-zero biases.
* **Vectorized Implementation:** A matrix-based framework for multi-observation training.
* **Global Convergence:** A 5,000-epoch experiment exploring local minima and the necessity of non-linear decision boundaries.

## 🛠️ Tech Stack
To ensure a pure understanding of the chain rule and optimization, **no ML frameworks (Keras, PyTorch, etc.)** were used:
- **Python 3.12**
- **NumPy:** Linear algebra and matrix operations.
- **Matplotlib:** Architecture diagrams and decision boundary visualizations.
- **Pandas:** Data management for training history.

## 🧪 Key Conclusions
1. **The Necessity of Hidden Layers:** Geometrically proves that XOR requires non-linear intermediate representations to be separable.
2. **Structural Gradient Freezing:** Identifies how specific input patterns (like $x=0$) can stall weight updates regardless of the learning rate.
3. **Non-Convex Optimization:** Demonstrates that even with 5,000 epochs, gradient descent can settle into a 50% accuracy local minimum depending on initialization.

---
**Author:** Elián David Martínez Orozco  
**Master's in Applied Statistics** - Universidad del Norte (April 2026).  
**Professor:** Dr. rer. nat. Humberto Llinás.
