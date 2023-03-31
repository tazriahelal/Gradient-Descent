# Gradient-Descent
Gradient Descent(From Scratch &amp; With tensorFlow)
### Let's start with a quiz here - 
![image.png](attachment:ff15f879-278b-4d70-8c65-3900557efd83.png)

I want to find the relationship function between x & y, so that the function describe the relationship between these two variable. 

The function is,`y = x * 2`

Again this, how about this one - 

![image.png](attachment:480fa2d5-6362-452c-b089-c545d1a47e56.png)

The function is,`y = x * 3`

Again this, how about this one - 

![image.png](attachment:d75855da-516c-49a9-ac6f-106b7a474cda.png)

The function is,`y = x * 2 + 3`

Again this, how about this one - 

![image.png](attachment:aeed0024-aa03-49e3-9c9b-ded7b0bc0bae.png)

Well this might be not that easy, Correct!
<h3>But</h3> if you give this to a computer, computer has a technique called a`Gradient Descent` . Using this technique it will find out the linear equation for this particular problem. The function is,`y = x * 0.5 - 1.5`

![image.png](attachment:5a89dd64-5eec-4c61-9b8a-60e39a06a65d.png)

**`y = x * 0.5 - 1.5` This is also called prediction function**. Means, in future if we change x values then y will change. That's the main point of Supervised Machine Learning technique or deep learning.

### Let's look a Insurance Datasets here-

![image.png](attachment:e6707c42-f450-42a9-b72d-c47a87c43795.png)

<h2>Binary Classification</h2> 

`Based on age & affordability, come up with a function that can predict if a person will buy insurance or not `

So here age and afforability is x & have_insurance is y or `y = f(x)` we are here trying to figure out this function f(x).

See here - 

![image.png](attachment:2f8affe1-8a3a-4888-ba5a-60a8d9676e2a.png)

Here it's a simple neural network with a single neuron. We have two input neurons but often we are talking about neural we don't take into consideration the input neurons hence this has only single neuron it's a logistic function. Logistic regression is a very simple case of a neural network having a singel neuron and in logistic regression there"are two components- one is ,<b> Weighted Sum </b> and another is <b> Sigmoid function </b>.

When we training a neural network, it should be remember that Gradient Descent is used during training of a neural network. SO Let's say, from above datasets, we have 13 data points, we will use all of this to train my network. So, I will feed the first sample,

![image.png](attachment:eae5180b-c4ff-4723-9b63-824710889b59.png)

I will initialize the weight to osme random value, here I do it as 1 and I will also initialize the bias which is here in zero and then we feed the first sample into the network, this is called `Forward Pass`.

![image.png](attachment:20b7b4ed-7d25-4a81-8395-91cd63547d7a.png)

For this sample it will be predicted value 0.99 & truth data is 0. So y is a predictcted value. Here we have the predicted value and the truth value. So, we will find the error value. 
So, the error is - 

<h2>error1 = -(truth value * log(predicted value) + (1 - truth value) * log (1 - predicted value)) = 4.6</h2>

for logistic regression we will use log loss, we don't use mean squared error or a mean absolute error. This is just a mathemetical equation for log loss. So, the first error comes to be a 4.6. Repeat this same process for all the samples in datasets.

<h2>Total Errors = sum of all the samples valuses in datasets</h2>

Then we calculate the Loss - 

![image.png](attachment:c44161a8-5aad-4757-8bc9-7e8985d0a823.png)

So, after the first epoch(Epoch is going through all training samples once, so here once we gone through training samples number 1 to 13 that means we have completed one epoch) which is 4.31. Then our goal is to back propagate the loss, so we can adjust the weight1(w1) and weight2(w2). It should be remember, whenever we train neural network we have to train multiple epoch until we get the correct value of weight1(w1) and weight2(w2). Now, the goal is adjust w1 & w2 in such a way so that my log loss is reduced  or less than 4.31. We can do this - w1 = w1 - adjust value, basically subtract or add some value with w1. So, what is the adjust value? We will do it using dervative. Like this - 

![image.png](attachment:e3819c40-08a4-454c-b1b5-62e302cb4691.png)

Learning rate usually 0.01, people assume, its just limiting the derivative fucntion. Here, ![image.png](attachment:8e004a8b-dfc1-4dcc-90d2-145c72f81cec.png) this shows the loss is changing for a given change in w1. Then we will find log loss derivative using this formula ![image.png](attachment:d2045865-4d78-48f4-8ece-0b933a1fcb08.png)

For bias - 

![image.png](attachment:ddfbdb8c-4a09-44ba-9cad-1eaf8a9e7e92.png)

We are using batch gradient descent actually. So, when should we stop to assume the weight value to training, we will stop when the error function is a convex function(its like a boat curve) or we found the global minima.

![image.png](attachment:3eb35737-3811-4b82-98df-bbc057444174.png)

we are doing derivative which is tangent here shown and trying to move point and get the global minima. **Lets move into code**
