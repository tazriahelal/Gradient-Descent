# Gradient-Descent
Gradient Descent(From Scratch &amp; With tensorFlow)
Gradient Descent, to put it simply, identifies the variables that minimize the cost function (error in prediction). Gradient Descent does this by iteratively moving in the opposite direction of the gradient toward a set of parameter values that minimize the function.

Let’s go over each stage of the gradient descent technique once more:

Repeat until convergence is reached:

 1. Determine the change in the parameters with the learning rate given the gradient.
 2. Recalculate the gradient using the new parameter value.
 3. Re-do step 1

### Gradient Descent Variants
Depending on how much information was utilized to determine the gradient, there are three types of gradient descent:

1. Batch Gradient Descent
2. Stochastic Gradient Descent
3. Mini-batch Gradient Descent

Batch Gradient Descent –
The error for each observation in the dataset is calculated via batch gradient descent, also known as vanilla gradient descent, however, an update is only made after all observations have been reviewed. Because the complete dataset must be kept in memory, batch gradient descent consumes a significant amount of processing resources.

Stochastic Gradient Descent –
For each observation, stochastic gradient descent (SGD) updates a parameter. As a result, it just requires one observation to update the parameter rather than looping through all of them. SGD is typically faster than batch gradient descent, however, because of its frequent updates, the error rate has a bigger variance and occasionally jumps instead of declining.

Mini-Batch Gradient Descent –
It combines stochastic gradient descent with bath gradient descent. A batch of observations receives an update thanks to mini-batch gradient descent. The batch sizes for this approach, which is preferred for neural networks, are typically between 50 and 256.
