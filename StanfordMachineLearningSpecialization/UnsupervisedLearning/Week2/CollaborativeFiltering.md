## Making Recommendations
* More used in academia than practical applications
* Used for recommending similar content in Amazon, Netflix, etc.
* Framework used:
  * ![Img](../../../Images/Pasted%20Graphic%2026%203.png)

## Using Per-item Features
* Have ratings for items in different categories
* For each user, they have different weights (depending on what they like) that make the algorithm output differently for different items
* ![Img](../../../Images/Pasted%20Graphic%2043.png)
* Cost function w/ regularization:
  * ![Img](../../../Images/Pasted%20Graphic%201%206.png)
* That is for one user. Now need to sum over all users:
  * ![Img](../../../Images/Pasted%20Graphic%203%208.png)

## Colaborative Filtering Algorithm
* Once have the parameters, can make predictions similar to linear regression, but now need to learn them
* Because we have training examples from different users, can come up with parameters
  * ![Img](../../../Images/Pasted%20Graphic%2044.png)
* Cost:
  * The cost function includes taking difference from each train example with the model and then adding in regularization term
  * Total cost function looks at all different movies and all different users to find all the parameters
  * ![Img](../../../Images/Pasted%20Graphic%201%207.png)
* Gradient Descent:
  * Function is of: $J(w,b,x)$ so we minimize all three variables
  * ![Img](../../../Images/Pasted%20Graphic%202%206.png)
* Based on how others rate a movie, can predict how others will rate something

## Binary Labels
* Different binary labels for different examples that have different use cases
  * ![Img](../../../Images/Pasted%20Graphic%203%209.png)
* Cost function
  * Now uses a binary cross entropy over all the training examples
  * ![Img](../../../Images/Pasted%20Graphic%204%207.png)