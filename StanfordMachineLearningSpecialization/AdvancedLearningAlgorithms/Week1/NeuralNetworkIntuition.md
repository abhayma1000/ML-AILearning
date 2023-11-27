## Welcome
* Learn about neural networks + decision trees. Used in industry
* Practical advice on ML
* Can use networks inference (predicting), then training

## Neurons and the Brain
* Neural networks want to mimic the behavoir of the brain
* Getting traction in late 1900s, but popular recently in speech recognition and image recognition
* Send output neurons to neurons who send output to other neurons, etc.
* Artificial NN is simplified version/mathematical model of actual network
* But, should get away from basis on the brain b/c we do not know much about the brain and our model is constantly evolving
* Data
  * More likely these days to have digital record vs. print
  * More data in total these days
  * Traditional AI (lin/log reg.) couldn't take advantage of lots of data
  * But, NN have better performance for lot's of data
  * ![Img](../../../Images/Pasted%20Graphic%2024.png)

## Demand Function
* Ex to see how NN works
* Demand problem is seeing how likely people are to want to buy a product
* Neurons:
  * Neuron takes input and predicts output like in log. reg. for ex
  * Wire a bunch of these units together
  * ![Img](../../../Images/Pasted%20Graphic%2025.png)
* Features:
  * Again, take in relevant features to predict
  * Go to input layer
* Connecting:
  * Connect inputs to more neurons to compute complex ideas that are useful and that combine features from the first layer
  * Combine neurons into layers that take similar features and output similar things
  * They then output to the next level until at output layer which is output of model
  * Each layer's neuron has input from every previous layers output
    * Then, it figures out which inputs there are relevant for the calculation
* ![Img](../../../Images/Pasted%20Graphic%2026.png)
* Hidden layers
  * Network determines itself what to calculate in middle, so don't need to explicitely tell
  * Data tells $X$ and $y$, but not about the layers in between. Those "hidden layers" are meant to be hidden and determined by the algorithm to get the correct $y$
  * Different architectures for NN. Choose # of hidden layers and # of neurons per each layer (can vary)
  * ![Img](../../../Images/Pasted%20Graphic%2027.png)

## Example: Recognizing Images
* Images can be broken into matrix and can unnroll into one vector
* Problem: Train network to take in this pixel brighness vector and output either person name, cat vs. dog, etc.
* ![Img](../../../Images/Face%20recognition.png)
* Layer purposes:
  * For images, first layer might be looking for different edges/lines
  * Next layer might be learning/grouping edge segments for parts of faces
  * Next might aggregate the face for detecting larger face shapes
  * Finally, how much a face corresponds to one in the database
  * We never tell it what to look for, it figures out what to look for
  * ![Img](../../../Images/Pasted%20Graphic%2029.png)