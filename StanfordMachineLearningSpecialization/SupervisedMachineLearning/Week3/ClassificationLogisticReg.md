## Motivations
* Classification where output variable can take only one of specified number of outputs
* Lin Reg not good for classification problems
  * Could use lin reg to fit a line, but would give a range in between 0-1. Could work, but outliers could skew the model and cause problems: ![Img](../../../Images/Pasted%20Graphic.png)
  * Logsitic regression gets rid of this problem and works well for classification
* Ex:
  * Spam email? yes or no
  * Fraudulent transaction? yes or no
* Binary classification: Two classes/output categories. 1/0, Yes/no, cat/dog, etc.

## Logistic Regression
* Most used classification algorithm
* Sigmoid function:
  * AKA Logistic function. Outputs values between 0 and 1. Follows function: $g(x) = \frac{1}{1 + e^{-z}}$ No matter z, always between the range 0-1
* Logsitic regression model:
  * $z = \vec{w}*\vec{x} + b$
  * $g(z)$ --> $0 < g(z) <1$
  * ![Img](../../../Images/Want%20outputs%20between%200%20and%201.png)
  * Intuition:
    * The output $g(z)$ is the probability that the class is (say 1). If $g(z)=0.7$ for 1, then 70% chance the true label y is 1

## Decision Boundary
* We have signmoid function, but how do we previct is output 0 or 1?
  * Can set a threshold over which we set $yhat=1$ or below: $yhat=0$. Reversing the sigmoid function, when $z<0$, then $yhat=0$ or $z>0$, then $yhat=1$
  * ![Img](../../../Images/Pasted%20Graphic%202%202.png)
* Decision boundary:
  * Equation for decision boundary is when $z=0$ because then $g(z)=0.5$
  * Line/curve where we are in between two classification groups. Left of one line --> one choice. Right --> other choice
    * ![Img](../../../Images/Pasted%20Graphic%203%202.png)
  * Can have non-linear decision curve and can come up with more complicated ones by having higher order input parameters to make weird looking decision boundaries
    * ![Img](../../../Images/Pasted%20Graphic%204.png)
    * ![Img](../../../Images/Non-linear%20decision%20boundaries.png)