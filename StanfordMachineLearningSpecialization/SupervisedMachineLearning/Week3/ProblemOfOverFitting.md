## Overfitting
* Overfitting + underfitting are problems but can be fixed
* Lin. Reg. example:
  * Can fit linear fit to quadratic data. Model underfits the training data (high bias)
  * Can fit a quadratic function, and it fits well. Generalization: Make good predictions on new data
  * Can fit a fourth order polynomial: $x^4$. Fits through all examples perfectly. Fits perfectly (cost function is zero), but isnt generalized to new data in that region (fits the data too well). Data overfitting, high variance
  * ![Img](../../../Images/Pasted%20Graphic%2013.png)
* Classification example:
  * Underfitting is simple linear fit that doesn't capture some aspects
  * Overfitting is again fitting every example
  * Just right is generalizing
  * ![Img](../../../Images/Pasted%20Graphic%2014.png)


## Addressing Overfitting
* Addressing overfitting:
  * Collect more training data
    * The curve starts to fit better
    * Data not always available though
    * ![Img](../../../Images/Collect%20more%20training%20examples.png)
  * Use less features
    * Use less $x^{(i)}$ ```for i in``` $\infin$
    * Less features means less weird curves that perfectly fit training data
    * Feature selection: pick the most relevant features
    * Might lose some information though that is useful
  * Regularization
    * Encourages algorithm to shrink values of parameters, but not zero
    * Use small values for the high order polynomials: $x^{>2}$

## Cost function with regularization
* Apply regularization through the cost function
* Make the parameters for high order x variables small
  * Instead of cost function, add the high order parameters onto the end of the already cost function
  * Minimizing this brings high order parameters close to zero
  * ![Img](../../../Images/Pasted%20Graphic%2017.png)
* Implementation
  * Just penalize all the parameters that are high. Add the lambda term to the end. Lambda called regularization paramter, like $a$ is a new parameter. Specifies importance of regularization
  * ![Img](../../../Images/Pasted%20Graphic%2016.png)
  * Lambda
    * If lambda is too big, then just a line. Penalizes all parameters $w$ and just $b$ left
    * If too small, then does nothing
    * ![Img](../../../Images/Pasted%20Graphic%2018.png)

## Regularized Linear Regression
* Same cost and everything as described above
* The derivative is different and adds the lambda term
* We do not regularize b, so $\partial{b}$ is same, but $\partial{w}$ is different
* ![Img](../../../Images/Pasted%20Graphic%2019.png)
* Steps:
  * ![Img](../../../Images/Pasted%20Graphic%2020.png)
  * ![Img](../../../Images/Pasted%20Graphic%2021.png)

## Regularized Logistic Regression
* Similar to the update for reg. lin. reg
* Add the lambda term to the end too to penalize the higher order terms
  * ![Img](../../../Images/Pasted%20Graphic%2022.png)
  * ![Img](../../../Images/Regularized%20logistic%20regression.png)