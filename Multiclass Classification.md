# Machine Learning
# Supervised Learning: Multiclass Classification

## What is Classification (Logistic Regression)

The classification problem is similar to the regression problem, except that the values we want to predict are a small number of discrete values. Classification can be binary or multiclass/multinomial.

### Multiclass Classification

Multiclass classification involves classifying data when we have more than 2 categories. Instead of y = {0,1} which we use in binary classification, we use y = {0,1,...,n}. 

### Multiclass Classification: One-vs-all

We divide the problem into n+1 (+1 because the index starts at 0) binary classification problems; in each one, we predict the probability that 'y' is a member of one of our classes.

<img width="255" alt="Multi Class Problem" src="https://user-images.githubusercontent.com/88804543/155815222-29c6444b-1622-44cf-af54-e0afb8f0cf0c.png">

Basically, we are choosing one class and then lumping all the others into a single second class. We repeat this multiple times, applying binary logistic regression to each case. Then use the hypothesis that returned the highest value as our prediction.

<img width="520" alt="Ex of 3 Class" src="https://user-images.githubusercontent.com/88804543/155815323-810dffc4-8424-41bf-8340-b292229a1b59.png">

Summary:

Train a logistic regression classifier h(x) for each class to predict the probability that y = i.

To make a prediction on a new x, pick the class that maximized h(x).





