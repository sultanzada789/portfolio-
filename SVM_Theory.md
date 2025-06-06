
# Support Vector Machine (SVM) - Theory

Support Vector Machine (SVM) is a powerful supervised learning algorithm used for classification and regression tasks. It aims to find the optimal hyperplane that best separates the data into classes.

## 1. What is SVM?

SVM is a **margin-based classifier** that attempts to find the **maximum margin hyperplane** (MMH) which separates data points of different classes.

## 2. Key Concepts

### a. Hyperplane

A hyperplane is a decision boundary that separates data into different classes.

**Example (2D case):**

![Hyperplane](https://upload.wikimedia.org/wikipedia/commons/7/72/SVM_margin.png)

### b. Margin

Margin is the distance between the hyperplane and the nearest data point from either class. SVM tries to maximize this margin.

### c. Support Vectors

Support Vectors are the data points that lie closest to the decision boundary. They are critical in defining the position and orientation of the hyperplane.

### d. Linearly Separable Case

If data is linearly separable, SVM finds a straight line (or hyperplane in higher dimensions) that perfectly divides the classes.

![Linearly Separable](https://upload.wikimedia.org/wikipedia/commons/2/2a/SVM_Concept.png)

### e. Non-Linearly Separable Case

When data is not linearly separable, SVM uses a **kernel trick** to project the data into a higher-dimensional space where a hyperplane can separate the classes.

![Kernel Trick](https://upload.wikimedia.org/wikipedia/commons/8/88/SVM_Kernel_Example.svg)

## 3. Kernel Functions

Common kernels include:

- **Linear Kernel:** `K(x, y) = x^T y`
- **Polynomial Kernel:** `K(x, y) = (x^T y + c)^d`
- **RBF (Gaussian) Kernel:** `K(x, y) = exp(-γ||x - y||²)`

## 4. Cost Function (Soft Margin)

When perfect separation is not possible, SVM uses a **soft margin** and introduces a regularization parameter `C` to allow misclassification:

`minimize (1/2)||w||² + C Σ ξ_i`  
subject to: `y_i (w^T x_i + b) ≥ 1 - ξ_i`, where `ξ_i ≥ 0`

## 5. Advantages and Disadvantages

### Advantages:
- Effective in high-dimensional spaces
- Works well with clear margin of separation
- Memory efficient

### Disadvantages:
- Not suitable for large datasets
- Less effective when classes overlap significantly
- Choosing the right kernel and parameters is crucial

## 6. Applications

- Image classification
- Text categorization
- Bioinformatics (e.g., cancer classification)

