# Assignment 3
## Framing-
ML systems learn how to combine input to produce useful predictions on never-before-seen data.

#### 1. Training
We feed in the labelled data for the model to learn the relationship between the features and labels. 
#### 2. Inference
The data fed to the model is inferred and useful predictions are made based on the relationships deribed from the training data set.
![image](https://user-images.githubusercontent.com/81459933/114316069-86a23180-9b1f-11eb-9e0c-7d0e03efd062.png)
![image](https://user-images.githubusercontent.com/81459933/114316113-c49f5580-9b1f-11eb-9549-32079ac35cc2.png)


## Descending into ML:
### Linear Regression
Data given to us can plotted and a straight line can be drawn where not all the points pass through all the points but substantially many points. . Using the equation for a line, you could write down this relationship as follows:
#### y'= w1x1 + b
1. y'= is the predicted label (a desired output)
2. b = is the bias (the y-intercept), sometimes referred to as w
3. w1 = is the weight of feature 1. Weight is the same concept as the "slope" m in the traditional equation of a line
4. x1 = is a feature (a known input)

Although this model uses only one feature, a more sophisticated model might rely on multiple features, each having a separate weight (w1, w2, etc.). For example, a model that relies on three features might look as follows:
#### y'= b + w1x1 + w2x2

### Training and Loss
1. Training a model simply means learning (determining) good values for all the weights and the bias from labeled examples. In supervised learning, a machine learning algorithm builds a model by examining many examples and attempting to find a model that minimizes loss; this process is called empirical risk minimization.
2. Loss is the penalty for a bad prediction. That is, loss is a number indicating how bad the model's prediction was on a single example. If the model's prediction is perfect, the loss is zero; otherwise, the loss is greater. The goal of training a model is to find a set of weights and biases that have low loss, on average, across all examples.

![image](https://user-images.githubusercontent.com/81459933/114316933-5a88af80-9b23-11eb-9642-5fcdd2804fef.png)

# Reducing Loss
An iterative approach is one widely used method for reducing loss, and is as easy and efficient as walking down a hill. 
![image](https://user-images.githubusercontent.com/81459933/115071945-8a192c80-9f14-11eb-990a-c3d58062f8ac.png)
Iterative strategies are prevalent in machine learning, primarily because they scale so well to large data sets.
The "model" takes one or more features as input and returns one prediction as output. To simplify, consider a model that takes one feature and returns one prediction: y'= b + w1x1
* b=0
* w1=0

Usually, we iterate until overall loss stops changing or changes extremely slowly. When that happens, we say that the model has converged.

## Gradient Descent
![image](https://user-images.githubusercontent.com/81459933/115086346-b0959280-9f29-11eb-8d7b-a2857e0c3728.png)
 1. We choose a random starting point and take the gradient of the curve at that point. 
 2. When there are multiple weights, the gradient is a vector of partial derivatives with respect to the weights.
 3. The gradient always points in the direction of steepest increase in the loss function. The gradient descent algorithm takes a step in the direction of the negative gradient in order to reduce loss as quickly as possible.
 4. To determine the next point along the loss function curve, the gradient descent algorithm adds some fraction of the gradient's magnitude to the starting point
 5. This process is repeated until the minima is obtained
 ![image](https://user-images.githubusercontent.com/81459933/115086637-47fae580-9f2a-11eb-9411-47f31e013138.png)


## Learning Rate
* Gradient descent algorithms multiply the gradient by a scalar known as the learning rate (also sometimes called step size) to determine the next point.
* For a very small learning rate, the process will take too long and consume computational power
* The Goldilocks value is related to how flat the loss function is. If you know the gradient of the loss function is small then you can safely try a larger learning rate, which compensates for the small gradient and results in a larger step size.

![image](https://user-images.githubusercontent.com/81459933/114316933-5a88af80-9b23-11eb-9642-5fcdd2804fef.png)

![image](https://user-images.githubusercontent.com/81459933/114316959-755b2400-9b23-11eb-887c-ec939086ff26.png)


![image](https://user-images.githubusercontent.com/81459933/114317005-ac313a00-9b23-11eb-87ba-ea70f549a267.png)

![image](https://user-images.githubusercontent.com/81459933/114317026-c539eb00-9b23-11eb-9ae4-b03ecfe2fb1e.png)

## Stochastic Gradient Descent
A large data set with randomly sampled examples probably contains redundant data. In fact, redundancy becomes more likely as the batch size grows. Some redundancy can be useful to smooth out noisy gradients, but enormous batches tend not to carry much more predictive value than large batches.

## Mini-Batch Stochastic Gradient Descent
Mini-batch stochastic gradient descent is between full-batch iteration and SGD. A mini-batch is typically between 10 and 1,000 examples, chosen at random. Mini-batch SGD reduces the amount of noise in SGD but is still more efficient than full-batch. Given enough iterations, SGD works but is very noisy. The term "stochastic" indicates that the one example comprising each batch is chosen at random.

![image](https://user-images.githubusercontent.com/81459933/114317041-d4209d80-9b23-11eb-9240-f2562f5b7027.png)


# Tensor Flow
## Introduction
TensorFlow APIs are arranged hierarchically, with the high-level APIs built on the low-level APIs. Machine learning researchers use the low-level APIs to create and explore new machine learning algorithms. First we increased the number of epochs sufficiently to get the model to converge and adjusting the learning rate. Lowering the learning rate while increasing the number of epochs or the batch size is often a good combination but the ideal combination is data dependent.
![image](https://user-images.githubusercontent.com/81459933/115124781-c1a1da80-9fe1-11eb-9dab-2f00d3d1d06a.png)

# Generalisation
This is the ability of the model to generalise the raw data. Increasing the complexity to suit the training data causes over-fitting leading to the decrease in performance of the model. 

# Training and Test Sets
We divide the data into 2 subsets
* Training set - A subset of data to train the model
* Test set - A subset of data to test the model

The test set must be large enough to give statistically meaningful results. It should reperesent the data set as a whole and should not have trends that differ form the training set or the data as a whole.

# Validation Set
Partitioning a data set into a training set and test set lets you judge whether a given model will generalize well to new data. However, using only two partitions may be insufficient when doing many rounds of hyperparameter tuning. Basically, we shuffle the data into different training sets so as to not let our model train specific to the characteristics of one particular kind of test set only.
![image](https://user-images.githubusercontent.com/81459933/115125210-370eaa80-9fe4-11eb-8be5-2064d13fc0e7.png)
# Representation
The data has certain parameters or features on which we will base our model. In order to train a model, we must choose the set of features that best represent the data. We should check that the feature isn’t noisy
![image](https://user-images.githubusercontent.com/81459933/115125444-b781db00-9fe5-11eb-9c81-22aaf34ff8c5.png)

# Feature Crosses
A feature cross is a synthetic feature formed by multiplying (crossing) two or more features. Crossing combinations of features can provide predictive abilities beyond what those features can provide individually.
However feature crosses between categorical features are sometimes more useful than numerical features. Thus we cross the one hot encodings of these features. From these crosses we get binary features that can be interpreted as logical conjunctions. From such feature crosses we get more predictive ability than either feature of their own.
![image](https://user-images.githubusercontent.com/81459933/115125506-25c69d80-9fe6-11eb-8f35-a185459a67f4.png)

# Regularization for Simplicity
Regularization means penalizing the complexity of a model to reduce overfitting.
We try to minimize both loss and the complexity. In this topic we analyze model complexity as a function of the weights of all the features in the model. We quantify complexity using the L2 regularization formula, which defines the regularization term as the sum of the squares of all the feature weights.
![image](https://user-images.githubusercontent.com/81459933/115125539-6b836600-9fe6-11eb-8af8-e8c2beb9fa35.png)
 ## Lambda
 When we perform L2 regularisation on a model, it encourges weight values toward 0 (but not exactly 0) and encourages the mean of the weights toward  0, with a normal (bell-shaped or Gaussian) distribution.
 Lowering the value of lambda tends to yield a flatter histogram
 When choosing a lambda value, the goal is to strike the right balance between simplicity and training-data fit:
 * If lambda value is too high the model will be simple, but risk of underfitting. 
 * If lambda value is too low, model will complex and risk of overfitting. The model won't be able to generalize to new data.

![image](https://user-images.githubusercontent.com/81459933/115125645-257ad200-9fe7-11eb-9a64-8a9ac8b586d6.png)
![image](https://user-images.githubusercontent.com/81459933/115125652-31669400-9fe7-11eb-8d55-7f9fa325c0dc.png)

# Logistic Regression
Instead of predicting exactly 0 or 1, logistic regression generates a probability—a value between 0 and 1, exclusive. The probability can be returned either as binary or as is. The sigmoid function produces output having those same characteristics.
 ![image](https://user-images.githubusercontent.com/81459933/115125686-7f7b9780-9fe7-11eb-92e8-615686454cc3.png)
  Without regularization, the asymptotic nature of logistic regression would keep driving loss towards 0 in high dimensions. If you don't specify a regularization function, the model will become completely overfit.
  
   # Classification
   
 In order to map a logistic regression value to a binary category, we have to define a classification threshold.
 A true positive is an outcome where the model correctly predicts the positive class. Similarly, a true negative is an outcome where the model correctly predicts the negative class. A false positive is an outcome where the model incorrectly predicts the positive class. And a false negative is an outcome where the model incorrectly predicts the negative class.  We can summarize the model using a 2x2 matrix containg the four possible outcomes namely true positive(TP), false positive(FP), true negative(TN), false negative(FN). Then evaluate classification models using metrics(accuracy, precision and recall) derived from these four outcomes.

## Accuracy
Accuracy is the fraction of correct predictions.
![image](https://user-images.githubusercontent.com/81459933/115125758-eb5e0000-9fe7-11eb-8af3-0dbd4ac1146b.png)
![image](https://user-images.githubusercontent.com/81459933/115125796-29f3ba80-9fe8-11eb-98ed-4a90347785f5.png)


## Precision
What proportion of positive identifications was actually correct.
![image](https://user-images.githubusercontent.com/81459933/115125781-0892ce80-9fe8-11eb-9cbc-5c2bf2507de3.png)
![image](https://user-images.githubusercontent.com/81459933/115125807-38da6d00-9fe8-11eb-8121-eb1ae6742e99.png)

# Regularization for Sparsity
In large data sets, certain low proability data values need to be set to exactly 0 which L2 does not do. Thus we introduced L1
![image](https://user-images.githubusercontent.com/81459933/115125858-9a9ad700-9fe8-11eb-8e0c-31f26b8b429b.png)
![image](https://user-images.githubusercontent.com/81459933/115125865-a25a7b80-9fe8-11eb-9c68-c33fe1a4e82a.png)



