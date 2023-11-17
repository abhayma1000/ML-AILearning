## Feature Scaling
* Problem:
  * For input values, can range from the 10s to 10,000...s
  * One axis can be on different scale than other axis
  * A gradient of the cost function is stretched in one direction
* Effects:
  * Gradient descent can bounce back in forth on smaller axis until find global minimum
* Solution: Scale the inputs
  * Make both inputs on a scale from 0-1
  * The dimensions are now comparable
  * ![Img](../../../Images/Pasted%20Graphic%201.png)
  * Rescaling speeds up gradient descent

## Implementing Feature Scaling
* Scale input values to comparable values to each other
* Can multiply each input value by a constant (divide by the max)
* Mean normalization:
  * $\frac{x_1 - \mu_1}{max - min}$
  * Gets values between: $-1<=x<=1$
  * ![Img](../../../Images/Pasted%20Graphic%203.png)
* Z-score normalization
  * Calculate mean and standard deviation ($\mu, \sigma)$
  * $\frac{x_1 - \mu_1}{\sigma_1}$, $\frac{x_2 - \mu_2}{\sigma_2}$, etc.
  * ![Img](../../../Images/Pasted%20Graphic%202.png)
* Rule of thumb
  * Try to get values around -1 to 1 (or in that general area). If already around that, leave alone
  * If too small: $1*10^{-...}$ then rescale too


## Checking for Grad Desc Convergence
* Working?
  * Job is to minimize cost function
  * Plot cost function $J$ at each update of the parameters and should get decreasing graph
  * If the function is decreasing after $\bold{every}$ iteration then it is working correctly
  * If starting to flatten the curve, then approaching final values
  * Hard to tell initially how much training to do
    * Can use automatic convergence test: If the cost decreased by less than some $\epsilon=10^{-3}$, then done
  
## Choosing learning rate $a$
* If cost is going down, up, down, etc., then gradient descent not working
  * Use smaller learning rate so it converges
  * Could also mean a bug in the code
* If learning rate too small, then takes forever to converge
* Use learning rates in multiples of 10: $0.001, 0.01, 0.1, 1$, etc.

## Feature Engineering
* Ex: Instead of using $width$ $x$ $depth$, can use the $ft^2$ comfined
  * Called feature engineering. Using knowledge of the problem to make life easier for the trainer
* Feature scaling is just scaling, feature engineering is changing it to be better for us


## Polynomial Regression
* So far been using straight lines, can now fit curves/non-linear functions
* Can artifically engineer features to linearize them so linearization works
  * Or, can add to the input data regular data + engineered to fit the curve
  * These are still using linear regression, just modifying input to be non-linear