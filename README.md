# Machine Learning Explained
An overview of machine learning and the mathematics powering machine learning

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
A contour plot is a graph that contains many contour lines. A contour line of a 2 variable function has a constant value at all points of the same line.
For fixed values of <img width="61" alt="theta0 theta1" src="https://user-images.githubusercontent.com/88804543/155757473-7b84b814-ee65-4a36-9013-0b3886f27c51.png">, is a function of x. This function of x is represented as: <img width="50" alt="Screen Shot 2022-02-25 at 9 10 26 AM" src="https://user-images.githubusercontent.com/88804543/155757715-6cc5eb1a-c5b2-46e2-8e53-67c9b7dd6d25.png">

<img width="161" alt="h of x function" src="https://user-images.githubusercontent.com/88804543/155759284-0178bc69-2e1b-4e30-b667-b3a5de4a5dab.png">

For <img width="93" alt="J thetas" src="https://user-images.githubusercontent.com/88804543/155757777-780dc40a-ab39-4e9f-9902-73fe48d96f45.png">, this is a function of the parameters <img width="61" alt="theta0 theta1" src="https://user-images.githubusercontent.com/88804543/155757844-ff4dad51-e98e-4f72-a872-24691005bf82.png">


<img width="641" alt="Contour Plot Example" src="https://user-images.githubusercontent.com/88804543/155760007-bc783eab-76ae-43a7-a9f1-72a740c98a85.png">

As you minimize the cost function, you get a corresponding theta0 and theta1. Those values of theta0 and theta1 are located at the center of the inner most 'circle' (on the 2D contour plot).

### Minimizing the Cost Function








## Machine Learning in Practice

Steps to run machine learning:
1. Collect/Gather the data
2. Prepare/Pre-process the data
3. Choose the optimal model
4. Train the model
5. Optimize the model
6. Make predictions
