# Machine Learning
# Supervised Learning: Classification

## What is Classification
The classification problem is similar to the regression problem, except that the values we want to predict are a small number of discrete values. Classification can be binary or multiclass/multinomial.

## Binary Classification
In binary classification, y can take on only two values: 0 and 1.

## Binary Classification Hypothesis Function
The hypothesis function is called the "Sigmoid Function" or the "Logistic Function".

<img width="145" alt="BC Hypothesis Function" src="https://user-images.githubusercontent.com/88804543/155811005-5e116908-319c-40da-9b4c-513739a1c94d.png">


<img width="574" alt="Sigmoid Function" src="https://user-images.githubusercontent.com/88804543/155811366-1104fd72-f416-42d7-9418-63c5aa64cd13.png">


##### The function g(z) maps any real number to the (0,1) interval.

h(x) will give us the **probability** that our output is 1. For example, h(x) = 0.80 give us a probability of 80% that our output is 1. The probability that our prediction is 0, is the complement of our probability that it's 1. So if the probability that it is 1 is 80%, then the probability that it is 0 is 20%.

<img width="320" alt="HofX Probability" src="https://user-images.githubusercontent.com/88804543/155811658-154444ab-a99c-4892-ab9e-d9f1fde797f6.png">


### The Decision Boundary

In order to get a discrete 0 or 1 classification, we can translate the output of the hypothesis function as follows:

<img width="171" alt="Screen Shot 2022-02-25 at 2 31 25 PM" src="https://user-images.githubusercontent.com/88804543/155811951-2308c36b-3fa6-4450-a00d-20ff4e9ec52a.png">

The way the logistic or sigmoid function (g) behaves is that when its input is greater than or equal to zero, its output is greater than or equal to 0.5:

<img width="93" alt="Logistic Function Behavior" src="https://user-images.githubusercontent.com/88804543/155812083-24c44223-20da-437e-a489-46e531b34eda.png">

Furthermore:

<img width="246" alt="Logistic Func Behavior2" src="https://user-images.githubusercontent.com/88804543/155812175-24223f2e-7b6c-4c36-a9b1-5d79748ecc62.png">

So if our input to g is <img width="41" alt="Theta Transpose X" src="https://user-images.githubusercontent.com/88804543/155812227-11151543-fa62-4833-8a00-b7428666ea3d.png"> (theta transpose X), then that means:

<img width="180" alt="Screen Shot 2022-02-25 at 2 35 17 PM" src="https://user-images.githubusercontent.com/88804543/155812267-a002f394-fc41-4770-ad65-1f41aa8a521d.png">

From the above, we can conclude:

<img width="152" alt="Screen Shot 2022-02-25 at 2 35 43 PM" src="https://user-images.githubusercontent.com/88804543/155812318-2882fd93-0761-4e5f-b67c-8450bec1fb52.png">

The Decision Boundary
The **DECISION BOUNDARY** is the line that separates the area where y = 0 and where y = 1. It is created by the hypothesis function.

<img width="272" alt="Screen Shot 2022-02-25 at 2 36 58 PM" src="https://user-images.githubusercontent.com/88804543/155812448-a8e57ec1-f2c4-43b0-bc2c-9d88d12ef561.png">

Note: the input to the sigmoid function g(z) does NOT need to be linear
