# MNIST Digit Classification Using Gaussian and GMM Classifiers

This project demonstrates the implementation of two probabilistic classifiers **from scratch** to classify handwritten digits from the [MNIST dataset](https://www.openml.org/d/554):

1. **Gaussian Classifier** – assumes each class follows a multivariate Gaussian distribution.
2. **GMM Classifier** – models each class as a **Gaussian Mixture Model (GMM)** with multiple components.

The project also visualizes the performance using **ROC curves** for all 10 classes.

---

## **Dataset**

- **MNIST** dataset (handwritten digits 0–9, 70,000 samples, 784 features per sample).
- Normalized to the range `[0,1]`.
- Sample size for training/testing: 30,000 samples (for faster experimentation).
- Train/Test split: 80% train, 20% test.

---

## **Project Structure**

- `GaussianClassifier`: Implements a multivariate Gaussian classifier.
  - Computes class-specific mean vectors and covariance matrices.
  - Predicts probabilities using the multivariate normal distribution.
- `SimpleGMM`: Implements the **Expectation-Maximization (EM)** algorithm for Gaussian Mixture Models.
  - Fits multiple components to a single class.
  - Computes log-likelihood for prediction.
- `GMMClassifier`: Wraps `SimpleGMM` for multi-class classification.
  - Computes class probabilities and predicts labels.

---

## **Key Features**

- Classifiers implemented **from scratch** (no `sklearn` classifiers used).
- Computes **class probabilities** for each test sample.
- Plots **ROC curves** and calculates **AUC** for all classes.
- Handles **numerical stability** issues (log-sum-exp trick, regularization).

---

## **Results**

Example outputs:

- **Gaussian Classifier Accuracy**: `~0.80`  
- **GMM Classifier Accuracy**: `~0.83`  

ROC curves are plotted for all classes to visualize model performance per digit.
