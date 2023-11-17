## Multiple features
* Before, we have used one feature, now we can use multiple features
  * More features gives more info to predict variables
  * Hold in a vector/array
  * New model (multiple linear regression):
    * $f_{w,b}(X) = w_1x_1+w_2x_2+w_{...}x_{...} + b$ = $\vec{w} * \vec{x} + b$ (dot product)
    * $w_1, w_2$, etc are how much a change in $x_1, x_2$ effects the output y
    * $\vec{w}$ vector for all w values but b is still just a number


## Vectorization
* Vectorized code makes lines shorter and more efficient computation
* Numpy is linear algebra library and array makes vectors
* Benefits of vectors
  * Without vectors: sums the product of $w_jx_j$ and this is done by iterating linearly
  * With vector, does things parallely and sums together, thus saving time
    * Ex: ```np.dot(w,x) + b```
* Runtimes
  * With vectorization, carries matrix multiplication simultaneously and adds in efficient way
  * Gradient descent:
    * w/o vectorization: update each weight individually over for loop with the derivatives
    * w/ vectorization: update each weight equal to derivative * learning rate simultaneously


## Grad Desc for Mult. Lin. Reg.
* $f_{w,b} = \vec{w}\vec{x} + b$. $J(\vec{w},b)$
* New update equations:
  * Use vectorized approach where $x$ and $w$ are vectors
  * ![Img](../../../Images/Screenshot%202023-11-15%20at%207.38.57%E2%80%AFPM.png)
  * ![Img](../../../Images/Screenshot%202023-11-15%20at%207.42.59%E2%80%AFPM.png)
* Alternatives to Gradient Descent
  * Another way to find $w$ and $b$ for linear regression
  * Normal equation method:
    * Advantage: No iterations, just one solve
    * Disadvantage: Only for linear regression