#  Logistic Regression

This folder explains Logistic Regression, one of the most important algorithms for classification problems in machine learning. It covers all key concepts including activation functions, loss functions, and optimizers.

---

## Topics Covered

1. Introduction
2. Activation Functions
3. Loss Functions
4. Optimizers
5. Evaluation Metrics

---


### 1. Introduction
Logistic Regression is mainly used for binary classification (Yes/No, 0/1, True/False).
It works by mapping input values to probabilities and then assigning them to a class.

### 2. Activation Functions
Activation functions transform linear inputs into non-linear outputs, often probabilities.

#### Sigmoid (Logistic Function):
- Outputs values between 0 and 1.
- Commonly used in Logistic Regression.
#### Tanh (Hyperbolic Tangent):
- Outputs values between -1 and 1.
- Centered around zero, often better for optimization than sigmoid.
#### ReLU (Rectified Linear Unit):
- Outputs positive values as-is, negatives as 0.
- Used widely in deep learning, not typically in Logistic Regression.
#### Leaky ReLU:
- Similar to ReLU but allows small negative values.
- Helps prevent “dead neurons.”
#### Softmax:
- Converts outputs into probabilities that sum to 1.
- Useful for multi-class classification problems.

---


### 3. Loss Functions
Loss functions measure how far predictions are from the actual values.

#### Binary Cross-Entropy Loss:
- Used in binary classification.
- Penalizes incorrect predictions more as confidence increases.
#### Categorical Cross-Entropy Loss:
- Used when there are more than two classes.
- Works with Softmax activation.
#### Mean Squared Error (MSE):
- Sometimes used, but not ideal for classification.
#### Hinge Loss:
- Commonly used in Support Vector Machines (SVMs).
- Can also apply to classification tasks.

---


### 4. Optimizers
Optimizers are methods that adjust weights to minimize the loss.

#### Gradient Descent:
- The most basic optimizer.
- Updates weights step by step in the direction that reduces loss.
#### Stochastic Gradient Descent (SGD):
- Uses one sample at a time to update weights.
- Faster but noisier than batch methods.
#### Mini-Batch Gradient Descent:
- Uses a small group of samples at a time.
- Balances speed and stability.
#### Momentum:
- Speeds up learning by considering past gradients.
- Helps escape local minima.
#### Adam (Adaptive Moment Estimation):
- Most popular optimizer.
- Combines momentum and adaptive learning rates.
#### RMSprop:
- Adapts learning rate for each parameter.
- Works well for recurrent and deep networks.

---


### 5. Evaluation Metrics

#### Accuracy: 
- Percentage of correctly classified samples.
#### Precision:
- Out of predicted positives, how many were correct.
#### Recall:
- Out of actual positives, how many were detected.
#### F1 Score:
- Harmonic mean of Precision and Recall.
#### Confusion Matrix:
- Table showing true positives, true negatives, false positives, and false negatives.

---


### Learning Outcomes

Understand the role of activation functions, loss functions, and optimizers in Logistic Regression.
Learn why sigmoid is commonly used but know alternatives for different cases.
Gain knowledge of how optimizers improve learning efficiency.
Be able to evaluate classification results with the right metrics.