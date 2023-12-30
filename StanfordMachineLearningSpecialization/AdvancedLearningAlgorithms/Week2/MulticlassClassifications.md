## Multiclass
* More than just two output labels, but still a discrete and set amount of labels
  * Like 0, 1, 3, etc. or classifying different animals
* Estimate that y is equal to the first class, second class, third class, etc.
* ![Img](../../../Images/Pasted%20Graphic%2013%202.png)

## Softmax
* Generalization of log. reg. (binary problem) to adapt to multi-class
* Softmax:
  * Calculate the output for each node/output class. ex: 4
  * Then, calculate the chance of y = that node by dividing by $\sum{}$ of all output
  * This then gives the probability of each node being the most likely
  * Choose the greatest one as the estimate
  * ![Img](../../../Images/Pasted%20Graphic%2014%202.png)
* Cost function for softmax:
  * Depending on the ground truth, $-log(y)$ where y is the ground truth. Therefore for all classes where it was wrong, high loss: $-log(1)$. Where it is right --> no loss
  * ![Img](../../../Images/Pasted%20Graphic%2015%202.png)

## NN with Softmax Output
* Put softmax into the output layer of the NN
* Add an output layer with number of units being number of classes
* Softmax diff from sigmoid, ReLU, etc. b/c it is now a function of all units, not just the single unit
* ![Img](../../../Images/Pasted%20Graphic%2016%202.png)
* Code
  * Use the SparseCategoricalCrossentropy loss function
  * ![Img](../../../Images/MNIST%20with%20softmax.png)

## Improved Impl of Softmax
* Better implementation of softmax compared to last video
* Different way that reduces numerical rounding and reduces error. Improves softmax therefore
* Instead of calculating a value, then rounding, then calculating again, can specify to "keep" this value and make more accurate
* Linear regression ex:
  * ![Img](../../../Images/Pasted%20Graphic%2018%202.png)
* For softmax, rearranges and computes more accurately
  * ![Img](../../../Images/Pasted%20Graphic%2019%202.png)
  * Therefore, because it is now a linear output, now need to change the ```model.predict()``` to now include the actual activation function in the last neuron
  * ![Img](../../../Images/Pasted%20Graphic%2020%202.png)

## Classification w/ Multiple Outputs
* Can have multiple output labels for a problem
  * Ex: Object recognition recognizing multiple objects (cars, busses, ppl)
* How do we do this w/ NN?
  * Can have 3 different NNs. One detect cars, one busses, one ppl
  * Can have 1 that detects all 3
    * Output layer has three nodes that are each sigmoid function. Probabilities that there are each thing
    * ![Img](../../../Images/Pasted%20Graphic%2021%202.png)