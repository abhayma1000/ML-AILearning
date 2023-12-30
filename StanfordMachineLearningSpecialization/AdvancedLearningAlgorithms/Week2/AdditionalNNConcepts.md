## Advanced Optimization
* Gradient descent is optimization algorithm, but now are others that are better at minimizing cost function
* Adam algorithm
  * If we are going in same direction and the learning rate is small, make the learning rate $a$ bigger
  * If $a$ is big and we are going back and forth, $a$ will decrease
  * ![Img](../../../Images/Pasted%20Graphic%2022%202.png)
  * Uses different learning rate for each parameter in the model
* Adam intuition
  * If parameter is moving in same direction, increase learning rate for that parameter. If it is oscillating, decrease $a$
  * ![Img](../../../Images/Adam%20Algorithm%20Intuition.png)
* Implementation
  * Need to set the initial learning rate, but then adjusts later on
  * ![Img](../../../Images/Pasted%20Graphic%2024%202.png)

## Additional Layer Types
* Have used dense type where get all activations from previous layer. Builds pretty powerful algorithms, but other types too
* Convolutional layer
  * Can have certain neurons only looking at parts of image
  * Why? Faster computation when don't need to look at everything. Also less prone to overfitting
  * ![Img](../../../Images/Pasted%20Graphic%2025%202.png)
* Convolutional NN
  * Can have network only take in what is "necessary"/what is important
  * ![Img](../../../Images/Convolutional%20Neural%20Network.png)
* People are trying to make more powerful layer types to make better networks
