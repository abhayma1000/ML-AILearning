## Forward Prop in a Single Layer
* Gets us intuition into what is happening in tensorflow
* Also, one day can come up with better model and need to know theory behind so can do this
* Calculations
  * For first layer:
    * Dot product the weights, input, and add b
    * Then apply sigmoid function
  * Second layer:
    * Dot product next weights, output from first layer, and add b
    * Then apply sigmoid function
  * Onwards
    * Keep on doing this calculations until at end of network
* This implementation hard codes for every neural. The dot product is for every neuron, but want to generalize for a layer (in next video)
* ![Img](../../../Images/Pasted%20Graphic%204%202.png)


## General Implementation of Forward Prop
* Not specific for every neuron, more generalized
* Generalizations
  * Weights $w$
    * Stack the weight vectors into a matrix. Weights matrix
    * Each column is weights for diff neurons
  * $b$
    * Puts all the $b$ in one-D vector
* ![Img](../../../Images/Pasted%20Graphic%205%202.png)
* Good to know what is going un under the hood


## Speculations on AGI
* Unclear path to Artificial General Intelligence, but can speculate how to get there
* ANI: Artificial narrow intelligence which does one task really well
  * Ex: Detecting digits, classification, etc.
  * Pretty much doing right now
* AGI
  * Do anything a human can do
  * Not really making as much progress that compared to ANI
  * Just because progress in ANI does not mean progress in AGI
* One learning algorithm hypothesis
  * Small handful of algorithms that are not specific but can generalize for many different problems
  * Parts of the brain are not just good for one thing, but can be taught to use different inputs too. General purpose parts
  * Human brains are surprisingly adaptable, so there should be one algorithm. Can we replicate this programming?
* Without pursuing AGI, NN and ANI is still powerful for applications