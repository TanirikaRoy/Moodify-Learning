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


