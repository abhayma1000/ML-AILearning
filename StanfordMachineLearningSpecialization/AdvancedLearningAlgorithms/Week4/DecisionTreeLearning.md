## Measuring Purity
* If all a single class, very pure. Somewhere in between, how pure is it? Entropy is measure of how impure
* Entropy is measure of how impure
  * Entropy vs. purity graph is parabolically shaped
  * ![Img](../../../Images/Pasted%20Graphic%2027%203.png)
  * ![Img](../../../Images/Pasted%20Graphic%2028%202.png)


## Choosign a Split for Info Gain
* Want to maximize purity so how to choose feature
* Different ways to split, how to choose
  * Calculate the entropy values first on the left and right sub-branches
  * Take a weighted average of the split and the entropy for each option. Do the entropy at the root node, then minus this weighted average
  * Called information gain
  * ![Img](../../../Images/Pasted%20Graphic%2029%203.png)
* Calculating information gain
  * ![Img](../../../Images/Pasted%20Graphic%2030%203.png)


## Putting it Together
* How to build a large decision tree
  * Start with training examples at root node and calculate information gain for all features
  * Pick feature with highest information gain
  * Split to right/left branches based on feature
  * Keep splitting until node is 100% one class, less than max depth, Info gain < threshold, # training examples is < threshold
  * ![Img](../../../Images/Pasted%20Graphic%2041.png)
* Recursive splitting
  * Works as recursive algorithm where checks if above splitting conditions are met first
  * Then finds feature with highest info gain and splits

## One Hot Encoding of Cat Variables
* One hot encoding
  * Instead of binary number for a feature or not, can make into categorical vector of whether have that feature or not
  * Only one feature is 1, the rest is 0
* ![Img](../../../Images/Pasted%20Graphic%201%205.png)

## Continuous Valued Features
* Features that can be any number
* Splitting
  * Need to split based on a finite number
  * Split based on number that gives highest information gain (information gain calculation needs to be done)
  * ![Img](../../../Images/Pasted%20Graphic%202%205.png)

## Regression Trees
* Predict a number
* Process
  * Split into different subgroups and at the final node, set the output regression to be the average of the training examples in that category
  * Split based on largest reduction in weighted variance (analagous to largest info gain)
  * ![Img](../../../Images/Pasted%20Graphic%203%206.png)
  * ![Img](../../../Images/Pasted%20Graphic%204%205.png)

