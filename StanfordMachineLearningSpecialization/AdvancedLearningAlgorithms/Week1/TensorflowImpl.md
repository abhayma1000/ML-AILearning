## Inference In Code
* Leading implementation of ML, along with PyTorch
* How can we implement inference in code and build forward propagation (calculate the output value from input)
* First layer is dense of the dimensions of the input
  * Dense is the name for regular layer of neural network
* Then second layer change the number of units and the activation function
* Each layer is a function $f(x)$ of the next layer
* ![Img](../../../Images/Pasted%20Graphic%205.png)


## Data in Tensorflow
* Different ways of representing matrices through tensorflow and numpy due to conflicting histories
  * Can convert ```tf.tensor``` to ```np.array``` and vice versa
* Numpy
  * Numpy stores data in vectors and matrices
  * Create matrices and vectors using ```np.array()```
  * ![Img](../../../Images/Pasted%20Graphic%201%202.png)
  * 1D vector for data

## Building a neural network
* Previously saw how to to forward propagation one layer at a time
* Build a NN
  * Create layers, but instead of manually passing data, create a Sequential to pass from one to another
  * ```model = Sequential([layer1, layer2])```
* Train
  * Make a training X dataset
  * Make a y outout training set
  * Do ```model.compile()``` to compile model after creating sequential
  * ```model.fit(x,y)``` to train the data to the dataset
* ```model.predict()``` carries out forward prop to calculate new value
* ![Img](../../../Images/Pasted%20Graphic%202%203.png)
* ![Img](../../../Images/Pasted%20Graphic%203%203.png)