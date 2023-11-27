## NN Implemented Efficiently
* Scale up to large networks by doing efficient vectorization. Done by matrix multiplication
* GPUs are good at large matrix multiplications
* Matrix mult
  * Multiply the input to the weights matrix and add the B and return that
  * ```np.matmul(A_in, W)```
  * Replaces the for loop for efficient forward propagation
* ![Img](../../../Images/Pasted%20Graphic%206%202.png)

## Matrix Mult Code
* Can transpose by: ```arr.T```
* Mat mult: ```np.matmult()```
* ![Img](../../../Images/Pasted%20Graphic%2015.png)
* NN implementaiton: ![Img](../../../Images/Pasted%20Graphic%201%203.png)