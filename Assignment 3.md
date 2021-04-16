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
. b=0
. w1=0

Usually, you iterate until overall loss stops changing or at least changes extremely slowly. When that happens, we say that the model has converged.

![image](https://user-images.githubusercontent.com/81459933/114316933-5a88af80-9b23-11eb-9642-5fcdd2804fef.png)

![image](https://user-images.githubusercontent.com/81459933/114316959-755b2400-9b23-11eb-887c-ec939086ff26.png)

![image](https://user-images.githubusercontent.com/81459933/114317005-ac313a00-9b23-11eb-87ba-ea70f549a267.png)

![image](https://user-images.githubusercontent.com/81459933/114317026-c539eb00-9b23-11eb-9ae4-b03ecfe2fb1e.png)

![image](https://user-images.githubusercontent.com/81459933/114317041-d4209d80-9b23-11eb-9240-f2562f5b7027.png)
