## Tensorflow Impl
* Need to specify the loss function to train on
* Then, call the fit function to fit the model to the data using the loss. Train for a specified number of $\bold{epochs}$ like 100
* ![Img](../../../Images/Train%20a%20Neural%20Network%20in%20TensorFlow.png)

## Training Details
* What the tf code is actually doing
* Create the model
* Specify the loss function for the network
* Then fit the $X$ -> $Y$ and for a set number of epochs
* ![Img](../../../Images/Pasted%20Graphic%203%204.png)
* Loss
  * When classifying 0 or 1, use ```binary cross entropy``` (same as log. reg.)
  * Syntax is to ```model.compile()``` using this BinaryCrossentropy
  * For lin. reg., use MeanSquaredError
  * Optimizing for $J(W,B)$ optimizes all parameters in W and B matrices
  * ![Img](../../../Images/Pasted%20Graphic%204%203.png)
* Gradient Descent
  * For every layer and neuron, update the $w$ and $b$ there from the derivative 
  * Derivatives
    * Tensorflow uses ```backpropagation``` algorithm automatically to calculate the derivatives
  * ```model.fit()``` trains and does all this
* ![Img](../../../Images/Pasted%20Graphic%205%203.png)
* When deep learning was young, implemented algorithms from scratch, but DL libraries are mature so can just reference their implementation. But useful to understand what's under the hood
* 