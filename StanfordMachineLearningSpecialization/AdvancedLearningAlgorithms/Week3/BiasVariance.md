## Diagnosing Bias and Variance
* To see bias and variance, look at how well it does on the training and validation/cross examination set
  * If underfit, (high bias) bad on training set and bad on val set
  * If overfit, good on training set and bad on val set
* ![Img](../../../Images/Pasted%20Graphic%2032%202.png)
* There is a curve between overfitting and underfitting
  * ![Img](../../../Images/Pasted%20Graphic%2033.png)

## Regularization and bias/variance
* How regularization can be implemented to reduce bias/variance
* Lin. reg. impl
  * Lambda part is added into the cost function
  * With high lambda value, underfits becuase all weights are punished
  * With low lambda value, overfits because no weights are ever punished
  * ![Img](../../../Images/Pasted%20Graphic%2034.png)
* Pick lambda
  * Pick which lambda best does on the cross validation set
  * Want to find a spot where it does both well on cross validation and train
* ![Img](../../../Images/Pasted%20Graphic%2035.png)


## Establish Base for Performance
* In order to judge training error, see how it is compared to human level performance
  * Because some problems are difficult for even humans (and sometimes a lot of noise)
  * If the gap is small, then good model
  * ![Img](../../../Images/Pasted%20Graphic%2036.png)
* There is healthy differences between baseline performance, training error, and cross validation error
  * ![Img](../../../Images/Pasted%20Graphic%2037.png)


## Learning Curves
* As you increase the training set size, the best error possible will increase. But, then cross validation error will decrease
  * This is because it has to fit to more training examples, therefore getting worse at each
  * For cross val, it gets better because more data means can generalize better
  * ![Img](../../../Images/Pasted%20Graphic%2038.png)
* Human level performance is a gap from both train and cv error
  * ![Img](../../../Images/Pasted%20Graphic%2039.png)
* High variance
  * Train performance better than human
  * ![Img](../../../Images/Pasted%20Graphic%2040.png)

## What to do next
* Couple ways to debug a learning algorithm
  * ![Img](../../../Images/Pasted%20Graphic%2023.png)

## Bias/Variance and NNs
* ![Img](../../../Images/Pasted%20Graphic%201%204.png)
* Bigger networks are low bias. If high bias, make bigger network
* If good on training and bad on cross val, get more data
* Sometimes, have things that conflict each other, hard to win at all things like Jtrain and Jcrossval
* ![Img](../../../Images/Pasted%20Graphic%202%204.png)
* With large network, when we reguralize, it will do same or better than smaller network (doesn't have to have high variance). Downsize is that it is computationally expensive
  * ONLY DOWNSIDE OF BIG NETWORK (AS LONG AS REGURALIZED) IS COMPUTATIONAL COST
  * ![Img](../../../Images/Pasted%20Graphic%203%205.png)
* Implementing NN reguralization
  * Decide the lambda per layer. Can keep constant
  * ![Img](../../../Images/Pasted%20Graphic%204%204.png)