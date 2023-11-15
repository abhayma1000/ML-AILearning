## Overview
* Trains the model to minimize $J(w,b)$, thus fitting the data
  * Can minimize any function, not just this cost function (even with >2 parameters)
* Outline:
  * 1. Start with some w,b
  * 2. Keep changing w,b to reduce $J(w,b)$
  * 3. Stop when settle near or at minimum
* Intuition:
  * Start at place on hills. You want to take a step downwards in the direction towards the minimum height
  * There are different ways to go down and can end at different minimum values (local minimas)

## Implementing
* Simultaneously Update w: $w := w-a\frac{d}{dw}J(w.b)$
  * $a$ is the learning rate which is a small number like 0.01. Controls how "big of a step" we are taking downwards. Aka how agressive gradient descent is
  * $\frac{d}{dw}J(w,b)$ tells which direction and size of step to take downhill
* Simultaneously Update b: $b := b - a\frac{d}{db}J(w,b)$
  * Same as w, but for b
  * Once get to the minimum, w,b won't change much
* Note: Make sure w is not updated before b because w is used in calculation of b:
  * ![Img](../../../Images/Screenshot%202023-11-15%20at%202.07.11%E2%80%AFPM.png)

## Intuition
* Partial derivative
  * $\frac{d}{dw}J(w)$ is the partial derivative of J(w)
  * Ex: When on the increasing side of a parabola cost function, derivative is positive, so $w-a*(pos_num)$ lowers w to get closer to min of parabola


## Learning Rate $a$
* Choice of $a$ has big impact on efficiency of gradient descent
* If $a$ is too small, gradient descent is slow and takes a while to get to minimum
* If $a$ is too big, gradient descent updates parameters by a lot and might overshoot the minimum, maybe increasing the cost function
* If at minimum, derivative is 0 and $w-0 = w$
* Gradient descent is proportional to derivative, but learning rate can amplify this by more or not


## Gradient Descent for Linear Regression
* As described before, use algorithm for w and b using the regression cost function
* Calculation of derivative
  * ![Img](../../../Images/Screenshot%202023-11-15%20at%204.29.31%E2%80%AFPM.png)
* Using the calculated derivative, we can update w and b:
  * $w := w - a\frac{1}{m}\Sigma_{i=1}^{m}(f_{w,b}(x^i)-y^i)x^i$
  * $b := b - a\frac{1}{m}\Sigma_{i=1}^{m}(f_{w,b}(x^i)-y^i)$
  * Squared error cost function will never have local minimum, just a local minimum
    * So long as learning rate is not too big, will always reach global minimum

## Running Gradient Descent
* Batch gradient descent is where on every step, look at all training examples instead of just subset