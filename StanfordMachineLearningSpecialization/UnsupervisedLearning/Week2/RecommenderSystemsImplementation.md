## Mean Normalization
* For recommender systems, more efficient algorithm if we normalize the ratings to have consistent values
* For each movie, calculate the average rating. Then subtract from each datapoint the averages per row
* This makes the system run faster and works for no-entry users
* ![Img](../../../Images/Pasted%20Graphic%206%206.png)

## Tensorflow Implementation
* Auto diff
  * We need to first initialize parameters to optimize
  * Then, manually create the function, cost function, and optimize usimg built in gradient descent
  * Called auto diff (auto grad) which does automatic differentiation. Not limited to just gradient descent though
  * ![Img](../../../Images/Pasted%20Graphic%207%203.png)
* ![Img](../../../Images/Pasted%20Graphic%208%204.png)
  * This optimizes the variables desired
  * We need to use this algorithm because it is not a dense layer, or other neural network types, so we have to manually implement the cost function, but use tf's differentiation technique

## Finding Related Items
* Finding related products or related movies to give to users
* Find others items with features similar to the other one
  * Use algorithm to find how similar
* ![Img](../../../Images/Pasted%20Graphic%209%204.png)
* Limitations
  * Hard to rank items and show something where the items are new and have few ratings
  * ![Img](../../../Images/Pasted%20Graphic%2010%205.png)
