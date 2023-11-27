## Neural Network Layer
* Layer of neurons make a network layer
* Process:
  * Input numbers
  * Neuron has parameters $\vec{w},b$ which output some activation function $g(\vec{w}*\vec{x}+b)$
    * Each neuron has different $\vec{w},b$ parameters
  * The output values of the neurons from the equation above are passed on to the next one and cycle continues
    * The output of the layer is the number of neurons there
  * ![Img](../../../Images/Pasted%20Graphic%2030.png)
* At the output node, can use binary classification. If $yhat>0.5$, then 1, otherwise 0
  * ![Img](../../../Images/Pasted%20Graphic%2031.png)

## More Complex Neural Networks
* In order to go from one layer to another layer
* Notation
  * $w,b,a$ all denoted by superscripts and subscripts denoting the layer number and and neuron within that layer
* ![Img](../../../Images/Pasted%20Graphic%2032.png)

## Inference/Predictions
* Called forward propagation to make predictions
* Handwritten digit example
  * Take in 8x8 b/w image with brightness values
  * Series of computation goes forward in the network and calculates for a new layer every time
  * In the end, label as either 0 or 1
  * 