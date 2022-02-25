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












