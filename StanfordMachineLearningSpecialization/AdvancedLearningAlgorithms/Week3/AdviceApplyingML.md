## What to do next
* What to do in a ML project that can make it better
* Debugging
  * Can try different things if large error
  * Get more training examples, smaller sets of features, additional features, polynomial features, decreasing $\lambda$, increasing $\lambda$
  * Can do diagnostics to see what is working/isn't working
    * Make good diagnostics before investing in getting more training examples or spending lots of time doing something
* ![Img](../../../Images/Pasted%20Graphic%2027%202.png)

## Evaluating a model
* Can help then improve the performance
* Can split the dataset into a say 70% training set and a 30% test set
* Can calculate the test error which is error over the test set and also calculate the training error
  * If you are overfitting the data, then the train loss will be low, but the test loss will be high
  * ![Img](../../../Images/Pasted%20Graphic%2028.png)

## Model Selection Cross Validation
* Technique to automatically choose good model for task
* Training error is not good measure of how good a model generalizes outside the training data (as described earlier)
* Model selection
  * Can choose linear model, quadratic, cubic, etc.
  * Choose which one gives lowest cost $J$ for test section
  * Flawed though
  * ![Img](../../../Images/Pasted%20Graphic%2029%202.png)
* New method
  * Split data into three: train, test, cross-validation
    * Can split train, cross val, test: 60%-20%-20%
  * All three have errors (calculated the same way). 
  * Use the cross validation (aka dev set) to choose which model is best
  * Then, use the test set to report to the outside world how good the model is
    * This makes the test set fair because we haven't changed anything from the test set. It is totally unbiased
    * If we use test set to choose which model, this makes the model biased for test set
  * ![Img](../../../Images/Pasted%20Graphic%2030%202.png)
  * Can also use to choose the network architecture: #nodes, #layers, etc.
* ![Img](../../../Images/Pasted%20Graphic%2031%202.png)