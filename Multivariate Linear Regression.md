# Machine Learning Explained
# Multivariate Linear Regression

## Linear Regression with Multiple Variables

Linear regression with multiple variables is known as "multivariable or multivariate linear regression".


### Multivariate Hypothesis Function

The notation for equations with multiple input variables:

<img width="392" alt="Multivariate Notation" src="https://user-images.githubusercontent.com/88804543/155785506-7915a519-6f01-4c87-8b5b-32c740efb61a.png">

The multivariable form of the hypothesis function accomodating multiple features looks like:

<img width="400" alt="Multivariate Hypothesis Function" src="https://user-images.githubusercontent.com/88804543/155785608-8f87b0b9-ee9f-4f15-b5d4-95c6fe498551.png">

To gain intuition about this function, it helps to think of each theta (theta0, theta1, ...) as an input feature.

Using the definition of matrix multiplication, the multivariable hypothesis function can be concisely represented:

<img width="405" alt="Multivariate Hypothesis Condensed" src="https://user-images.githubusercontent.com/88804543/155785922-e82e838c-c66c-443b-81ba-c9ec633adf71.png">

Note: for convenience reasons, we can assume:

<img width="213" alt="Multivariate Assumption" src="https://user-images.githubusercontent.com/88804543/155786004-38f33199-2d86-4097-a913-547ce880ec9f.png">

- This allows us to do matrix operations with theta and x. Hence making the two vectors 'theta' and 'x(i)' match each other element-wise (meaning they have the same number of elements: n + 1).

### Gradient Descent for Multiple Variables

The gradient descent equation itself is generally the same form as before (for linear regression with one variable); we just have to repeat it for 'n' features:








