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


### Hypothesis Function & Adding Features

We can improve our features and the form of the hypothesis function in a couple different ways. We can combine multiple features into one. For example, we can combine x1 and x2 into a new feature x3 by multiplying x1 and x2.

If a linear hypothesis does not fit the data well, we can change the behavior or curve of our hypothesis function by making it a quadratic, cube, or square root function (or any other form).

<img width="922" alt="Screen Shot 2022-02-25 at 1 57 33 PM" src="https://user-images.githubusercontent.com/88804543/155808661-99534d3c-2be0-4252-be66-5b0b851715f7.png">

In the cubic version, we created new features: x2 and x3. Where:

<img width="89" alt="Screen Shot 2022-02-25 at 2 00 15 PM" src="https://user-images.githubusercontent.com/88804543/155808937-861d9bdf-18d2-45c7-b2c9-72b113030105.png">

<img width="94" alt="Screen Shot 2022-02-25 at 2 00 20 PM" src="https://user-images.githubusercontent.com/88804543/155808951-cd8ca080-5c36-43ff-bdf5-a64d5504f93b.png">


To make it a square root function we could do: <img width="255" alt="Add Square root" src="https://user-images.githubusercontent.com/88804543/155809430-3926a728-f189-4f03-a35d-f9dadee60afd.png">


An important thing to keep in mind is, if you choose your features this way then feature scaling is critical. 


### Gradient Descent for Multiple Variables

The gradient descent equation itself is generally the same form as for linear regression with one variable; we just have to repeat it for 'n' features:

<img width="326" alt="Multivariate Gradient Descent" src="https://user-images.githubusercontent.com/88804543/155803881-3c0cd353-b3bb-4ec1-b9b8-7adfd8cfa5f0.png">

To condense it:

<img width="464" alt="Multivariate Gradient Descent Condensed" src="https://user-images.githubusercontent.com/88804543/155803955-e53ca351-22c0-417b-9674-f64c1f884a3b.png">


### Gradient Descent - Increasing Speed

We can increase the speed of gradient descent by having each of our inpu values in roughly the same range. This is because theta will descend quickly on samll ranges and slowly on large ranges. So gradient descent will oscillate down to the optimum when the variables are very uneven. To prevent slow gradient descent, we can modify the ranges of our input variables so they are all roughly the same. Ideally, the input variables should be:

<img width="117" alt="Ideal Input Value Range" src="https://user-images.githubusercontent.com/88804543/155804339-4e85aed9-51fd-4b43-bd4a-a46c758c50cf.png">

Note: these are not exact requirements; this is an attempt to speed up gradient descent

Two techniques to get the input values into the ideal ranges are:
1. Feature Scaling
2. Mean Normalization

#### Feature Scaling
Feature scaling involves dividing the input values by the range (or standard deviation) of the input variable. The range would be the maximum value minus the minimum value of the input variable.

#### Mean Normalization
Mean normalization involves subtracting the average value for an input variable from the values for that input variable resulting in a new average value for the input variable of just zero. 

Implementing both feature scaling AND mean normalization would look like:

<img width="160" alt="Feature Scaling and Mean Norm" src="https://user-images.githubusercontent.com/88804543/155806722-8e699630-1224-4ddd-bf30-9fb76e924db6.png">

where

<img width="29" alt="Screen Shot 2022-02-25 at 1 40 12 PM" src="https://user-images.githubusercontent.com/88804543/155806789-315899eb-7a56-48fe-8d02-454a8a4c84f2.png"> = average of the values for feature (i)

<img width="31" alt="Screen Shot 2022-02-25 at 1 41 13 PM" src="https://user-images.githubusercontent.com/88804543/155806914-d965da4b-584b-484d-bbc5-d1ed1c00e86b.png"> = the range of values (max -min) OR the standard deviation for feature (i)


### Gradient Descent - Learning Rate

Ensuring you have selected an appropriate learning rate (alpha) can be tested by making a plot with the **number of iterations of gradient descent on the x-axis** and the **cost function, J(theta), on the y-axis**. 

If J(theta) ever increases --> then decrease alpha

It has been proven that if the learning rate alpha is sufficiently small, then J(theta) will decrease on every iteration.

But if alpha is TOO SMALL, gradient descent can be slow to converge.

If alpha is TOO LARGE, gradient descent may not decrease on every iteration and thus may not converge

