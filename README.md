# Logistic Regression From Scratch

I built this small project to understand how logistic regression works internally.  
Instead of using scikit-learn’s LogisticRegression, I wrote the full training logic myself using only NumPy.

# Dataset
I generated a simple two-class dataset using make_blobs. Each sample has two features because it makes it possible to plot the data and the final separating line. The clusters are placed far enough apart so that a straight line can separate them.

# What I Implemented
I coded the sigmoid function, the binary cross-entropy loss, and the gradient descent update rule.  
The model starts with weights set to zero and updates them 1000 times.  
During training, I printed a few cost values to ensure the loss was going down.

# What the Learned Weights Mean
After training, the model gave the following parameters:

W1 = 1.6379374603657055  
W2 = -0.404411072106562  
b  = 0.1962176434408345

The dataset created by make_blobs is mostly separated horizontally.  
Because of that, the first feature contributes more to the class separation.  
That explains why W1 ended up with a larger value than W2.  
The sign of W2 being negative means the decision boundary tilts upward when you plot it.

The slope of the separating line comes from the ratio -W1/W2.  
This matches the way the clusters appear visually.

# ASCII Sketch of the Boundary
Below is a rough text sketch of how the data looked before plotting:

                x   x   x   x
            x   x   x
        x   x

-------------------------------------  separating line

      x    x
   x    x    x

The upper group represents one class and the lower group the other.

# Files
The project includes:
- a Python file containing the complete implementation  
- two PNG images saved during execution (cost plot and decision line)  
- a text file with the final numeric results

My goal with this project was simply to understand the math and see the result visually rather than rely on a library.
