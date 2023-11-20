## Cost Function For Logistic Regression
* Cost function gives a way to measure how well parameters fit training data
* Squared error cost function not good for log. reg.
  * Cost function will be non-convex (not smooth) for classification. Gradient descent would get stuck on different local mins
  * Different cost function makes grad. desc. reach global min
* Cost vs. Loss
  * Loss is the part of cost where take individual sample. How are we doing on that example:
  * ![Img](../../../Images/Pasted%20Graphic%206.png)
  * Cost is overall
* Loss for logistic reg:
  * Use log equation
  * If the answer is really off (close to 0 when actually 1 or vice versa), then loss increases exponentially. Loss at the right answer is close to 1
  * ![Img](../../../Images/Pasted%20Graphic%207.png)
* Cost put together:
  * ![Img](../../../Images/Pasted%20Graphic%208.png)

## Simplified Cost Func for Log Reg
* Simpler way to write out loss + cost function to make it easier to implement gradient descent
* Equation:
  * ![Img](../../../Images/Pasted%20Graphic%209.png)
  * Equivalent to the less complex formula
  * $y^i$ is either 0 or 1, so one side of the equation cancels out and same as other formula
* Cost
  * Average of the loss across the training set of m examples
  * ![Img](../../../Images/Pasted%20Graphic%2010.png)
* Why this Cost function?
  * Derived from statistics called maximum likelihood
  * This function is convex: has single global minimum