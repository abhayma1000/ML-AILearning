## Alternatives to Sigmoid Activation
* Can use others to make a more powerful network
* ReLU $g(z) = max(0, z)$ is popular
* ![Img](../../../Images/Pasted%20Graphic%206%203.png)
* Can now build variety of networks

## Choosing Activation Function
* Depending on the output, choose the activation function. Also for the hidden layers too
* Output layer
  * Choose based on problem solving
  * For binary classification, sigmoid function because it is between 0-1
  * For regression problem, can choose something like just linear/no activation function
    * Therefore, output can be any real number
    * But depends on problem
  * For regression problem where need only positive number, can use ReLU
  * ![Img](../../../Images/Pasted%20Graphic%207%202.png)
* Hidden layers
  * ReLU is most common in hidden layers. Benefits:
    * ReLU is pretty fast to compute. Just max. Compared to sigmoid which is slower
    * Also ReLU has only one flat section. Better than sigmoid which has two. Helps with gradient descent optimizing more quickly
  * ![Img](../../../Images/Pasted%20Graphic%208%202.png)
* ![Img](../../../Images/Choosing%20Activation%20Summary.png)

## Why Activation Functions
* With no activation function, every layer just becomes a linear regression model and cannot learn anything more complex. Ruins purpose of NN
* Basically, w/o activation functions, it compounds the $wx+b$ with the next $wx+b$ so that it is just one linear function in the end
  * Don't use linear activation function in hidden layers
* ![Img](../../../Images/Pasted%20Graphic%2010%202.png)
* ![Img](../../../Images/Pasted%20Graphic%2011%202.png)
* ![Img](../../../Images/Pasted%20Graphic%2012%202.png)
