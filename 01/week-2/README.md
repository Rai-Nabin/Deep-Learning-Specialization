# Neural Network Basics
**Vectorization:**

- Neural network implementations aim to process the entire training set without explicit for-loops, using vectorization techniques.
- This significantly speeds up computation.

**Forward and Backward Propagation:**

- Neural network computations are organized into a forward pass (forward propagation) and a backward pass (backward propagation).
- Forward propagation calculates predictions, and backward propagation calculates gradients for parameter updates.

### Logistic Regression for Binary Classification
![Binary Classification](./images/01-binary-classification.png)

**Problem Setup:**
- Binary classification aims to categorize inputs (e.g., images) into two classes (e.g., cat or non-cat).  
- The output label (y) is either 0 or 1.

**Image Representation:**
- Images are stored as three matrices representing red, green, and blue color channels.  
- These matrices are "unrolled" into a single feature vector (x).  
- For a 64x64 pixel image, the feature vector has a dimension of 12,288 (64x64x3).
- n<sub>x</sub> represents the dimention of the input feature vector x.

**Notation:**
- (x, y): A single training example, where x is the feature vector and y is the label.
- m: The number of training examples.
- m<sub>train</sub>: alternative notation to represent the number of training examples.
- m<sub>test</sub>: the number of test examples.
- X: A matrix formed by stacking the training example feature vectors (x<sub>1</sub>, x<sub>2</sub>, ..., x<sub>m</sub>) as columns.
    - Dimensions: n<sub>x</sub> by m.
    - `X.shape` in python returns (n<sub>x</sub>, m).
- `Y`: A matrix formed by stacking the training example labels (y<sub>1</sub>, y<sub>2</sub>, ..., y<sub>m</sub>) as columns.
    - Dimensions: 1 by m.
    - `Y.shape` in python returns (1, m).

