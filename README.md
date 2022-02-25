# Machine Learning Explained
An overview of machine learning and the mathematics powering machine learning.

Continue reading here to learn about machine learning for **linear regression with one variable** and general info about machine learning. 

See [Multivariate Linear Regression](https://github.com/jordanlevy001/Machine-Learning-Explained/blob/main/Multivariate%20Linear%20Regression.md) to learn about machine learning for multivarite linear regression

## Two Types of Machine Learning
1. Unsupervised
2. Supervised

## Unsupervised Learning
Unsupervised learning is used when you don't yet know the questions you are asking of your data. You would like to identify patterns or similar groups within the data, but you don't know what those might be.

## Supervised Learning
Supervised learning is used when you do know what you want to identify within your data. It's used when you know what your output should be. Supervised learning can be divided into its two most popular techniques: regression and classification. Regression is used to predict continuous variables. Whereas classification is used to predict discrete outcomes. Features are the variables used to inform the prediction. The target/output is the predicted outcome.

In supervised learning, a model is initiated or a template for the algorithm is created. Then it will analyze the data and attempt to learn patterns, which is also known as fitting and training. After the data has been fit and trained, the model will then make predictions.

### Supervised Learning Techniques: Regression & Classification

### Regression
When the target variable to predict is **continuous**, then the learning problem is considered a regression problem.

### Classification
When the target variable to predict is **discrete**, then the learning problem is considered a classification problem.


## Linear Regression with One Variable - Cost Function

Using a cost function, we can measure the accuracy of our hypothesis function. This takes an average difference of all the results of the hypothesis with inputs from 'x' and the actual outputs (y).

<img width="462" alt="Cost Function" src="https://user-images.githubusercontent.com/88804543/155618200-9f364b61-b14e-4fa3-82f4-f583d2572d00.png">

The cost function, broken down, is 1/2 of the mean of the squares of the difference between the predicted value (<img width="50" alt="h of x" src="https://user-images.githubusercontent.com/88804543/155762736-7851d434-6420-4900-8926-83413aec7dab.png">) and the actual value (y).





<img width="1140" alt="Learning Problem Diagram" src="https://user-images.githubusercontent.com/88804543/155622664-1920b3a0-aabb-4fc7-a888-cebb450c79cf.png">


#### Linear Regression with One Variable - Cost Function & Contour Plot


<img width="692" alt="hypothesis and cost function" src="https://user-images.githubusercontent.com/88804543/155769286-bc008098-a4a1-4ee4-8275-e5b933659294.png">


A contour plot is a graph that contains many contour lines. A contour line of a 2 variable function has a constant value at all points of the same line.
For fixed values of <img width="61" alt="theta0 theta1" src="https://user-images.githubusercontent.com/88804543/155757473-7b84b814-ee65-4a36-9013-0b3886f27c51.png">, is a function of x. These <img width="61" alt="theta0 theta1" src="https://user-images.githubusercontent.com/88804543/155757473-7b84b814-ee65-4a36-9013-0b3886f27c51.png"> are considered parameters of the model, and x is the independent variable.

This function of x is represented as: <img width="50" alt="Screen Shot 2022-02-25 at 9 10 26 AM" src="https://user-images.githubusercontent.com/88804543/155757715-6cc5eb1a-c5b2-46e2-8e53-67c9b7dd6d25.png">

<img width="161" alt="h of x function" src="https://user-images.githubusercontent.com/88804543/155759284-0178bc69-2e1b-4e30-b667-b3a5de4a5dab.png">

For <img width="93" alt="J thetas" src="https://user-images.githubusercontent.com/88804543/155757777-780dc40a-ab39-4e9f-9902-73fe48d96f45.png">, this is a function of the parameters <img width="61" alt="theta0 theta1" src="https://user-images.githubusercontent.com/88804543/155757844-ff4dad51-e98e-4f72-a872-24691005bf82.png"> . Plotted as a 3D and corresponding 2D contour plot:

<img width="641" alt="Contour Plot Example" src="https://user-images.githubusercontent.com/88804543/155760007-bc783eab-76ae-43a7-a9f1-72a740c98a85.png">

As you minimize the cost function, you get a corresponding theta0 and theta1. Those values of theta0 and theta1 are located at the center of the inner most 'circle' (on the 2D contour plot).


### Minimizing the Cost Function

How do we choose the parameters theta0 and theta1 so that h(x) is as close to the actual value (y) as possible? In other words, the value we predict ( h(x) ) on the input value (x) that is least close to the actual value (y) for the examples in the training set (x,y). Remember the cost function measures the accuracy of our hypothesis function.

So we need to minimize over theta0 and theta1. We want the difference between our predicted and actual outcomes to be as small as possible. So we want to sum over the training set i = 1 to m (m = the # of training examples. Using the notation:

<img width="95" alt="xi yi" src="https://user-images.githubusercontent.com/88804543/155765280-9cb3354a-8b28-4662-90f1-9f673d9dd255.png">

where i is the ith training example.

Looking above at the contour plot of J(theta0, theta1) above, we want to find the minimum value of J(theta0, theta1), which is the smallest oval (global minimum) in the 2D contour plot. Once we have the contour plot, we can use a method such as ordinary least squares or **GRADIENT DESCENT** to find the minimum of J(theta0, theta1). Once we have the minimum values of theta0 and theta1, those values are used for h(x) and the regression line is plotted to the training data.


### Gradient Descent For Linear Regression
Gradient descent specifically applied to the case of linear regression:

<img width="480" alt="Gradient Descent for linear regression" src="https://user-images.githubusercontent.com/88804543/155771835-4f4d0708-9dba-4389-b216-8041e5501c18.png">

where

m = the size of the training set

theta0 is a constant that will be changing simultaneously with theta1

x(i), y(i) are values of the given training set (data)


### Gradient Descent in General

Gradient descent is an efficient function to find the minimum values of J(theta0, theta1). This method is used in linear regression and other machine learning algorithms. Gradient descent will start at a point (theta0, theta1), and take small steps to try to find the local minimum. If we start at a different point, we may end up a at a different local minimum. 

The gradient descent algorithm:

<img width="386" alt="Gradient Descent Algorithm" src="https://user-images.githubusercontent.com/88804543/155769525-a51f4451-1a43-46bf-9222-5b143d2eea3b.png">

where:

j = 0,1 represents the feature index number

alpha = the learning rate

At each iteration j, one should simultaneously update the parameters: theta1, theta2, theta3, ..., theta n
Updating a specific parameter prior to calculating another one on the j(th) iteration would yield the wrong implementation

#### The Learning Rate
We should adjust the parameter alpha (the learning rate) to ensure the gradient descent algortihm converges in a reasonable amount of time. Failture to converge or too much time to obtain the minimum value implies that our step size is incorrect.

If alpha is too small, gradient descent will be very slow.

If alpha is too large, gradient descent can overshoot the minimum. It may fail to converge, or even diverge.

Gradient descent can converge to a local minimum, even with a fixed learning rate alpha. As gradient descent approaches a local minimum, it will automatically take smaller steps. So there is no need to decrease alpha over time.

#### Example of Gradient Descent on a Quadratic Function

<img width="307" alt="Ex Grad Descent on Quad Func " src="https://user-images.githubusercontent.com/88804543/155772327-96dd0d91-f2cd-4359-8dfd-9534e1c36288.png">

The ellipses shown in the image above are the contours of a quadratic function. The blue line shows the trajectory taken by gradient descent, which was initialized at (48,30). The x's joined by straight lines, mark the successive values of theta that gradient descent went through as it converged to the minimum.


## Machine Learning in Practice

Steps to run machine learning:
1. Collect/Gather the data
2. Prepare/Pre-process the data
3. Choose the optimal model
4. Train the model
5. Optimize the model
6. Make predictions
