"""
Cost Function Intuition — Linear Regression
-------------------------------------------

This file summarizes how the cost function helps choose the best parameter(s)
in linear regression.

Model:
    f(x) = w*x + b

Goal:
    Find w and b that minimize the cost function J(w, b).

Cost Function:
    J(w, b) = (1 / (2m)) * Σ( f(x_i) - y_i )^2

We want:
    minimize J(w, b)

Simplified Model (b = 0):
    f(x) = w*x
    J(w) = (1 / (2m)) * Σ( (w*x_i - y_i)^2 )

Training Data:
    (1,1), (2,2), (3,3)

Cost Example for Different w Values:

1. w = 1
    f(1)=1, f(2)=2, f(3)=3
    Errors = 0
    J(1) = 0

2. w = 0.5
    Errors:
        (0.5 - 1)^2
        (1 - 2)^2
        (1.5 - 3)^2
    Sum = 3.5
    J(0.5) = 3.5 / 6 = 0.58

3. w = 0
    Errors:
        1^2 + 2^2 + 3^2 = 14
    J(0) = 14 / 6 ≈ 2.33

4. w = -0.5
    Gives large errors
    J(-0.5) ≈ 5.25

Intuition:
    - Each value of w gives a different straight line f(x).
    - Each line produces a corresponding cost J(w).
    - Plotting J(w) shows a curve; minimum point is the best w.
    - Best value in this example: w = 1.

General Case:
    When using w and b, J(w,b) forms a 3D surface.
    Linear regression finds w and b values that minimize the cost.

"""

# Optional: example cost function implementation
import numpy as np

def compute_cost(x, y, w):
    """
    Compute J(w) for the simplified model f(x) = w*x
    """
    m = len(x)
    predictions = w * x
    errors = predictions - y
    cost = (1 / (2 * m)) * np.sum(errors ** 2)
    return cost

if __name__ == "__main__":
    # Example data
    x = np.array([1, 2, 3])
    y = np.array([1, 2, 3])

    for w in [1, 0.5, 0, -0.5]:
        print(f"w = {w}, cost = {compute_cost(x, y, w)}")
