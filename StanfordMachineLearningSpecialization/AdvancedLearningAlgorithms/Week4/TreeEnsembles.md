## Using Multiple Decision Trees
* Weakness of one decision tree is can be sensitive to small changes in data
* Can make multiple (tree ensemble)
* A new training example can change info gain and make a new feature the best to split on
* ![Img](../../../Images/Trees%20are%20highly%20sensitive%20to%20small.png)
* Tree ensemble
  * Train multiple trees
  * Run new example on all trees and get them all to vote on which is most likely right answer
  * ![Img](../../../Images/Pasted%20Graphic%2042.png)
* Reason for ensemble
  * To have many decision trees and have them all vote makes it less seceptable to changes in training data/new examples
  * How to come up with different trees though?

## Sampling w/ Replacement
* Sampling w/ replacement is choosing four but putting back in so can have duplicates
  * ![Img](../../../Images/Sampling%20with%20replacement.png)
* Example
  * Sample 10 from training set of size 10 w/ replacement so can get random (w/ repeats) of that training set
  * ![Img](../../../Images/Sampling%20with%20replacement%202.png)

## Random Forest Algorithm
* Random Forest algorithm to build a tree ensemble
* Process:
  * For 1 to B times:
    * Use sampling w/ replacement to create new training set
    * Train the decision tree using new dataset
  * B is usually $= 64 to 128$. After too much, diminishing returns w/ slower computations
  * Sometimes often end up with same root node feature. So, can randomize the feature at root node to make different trees
    * Out of n features, pick random subset and allow algorithm to only pick from that subset
* ![Img](../../../Images/Pasted%20Graphic%204%206.png)

## XGBoost
* Quick, open source way to build decision tree ensembles. Most common
* Bossting
  * When building next decision tree, focus on the subset that is not doing well on
  * Pick misclassified examples from previously trained trees
  * ![Img](../../../Images/Pasted%20Graphic%205%205.png)
* XGBoost
  * Open source, fast, good default boosting algorithm. Used a lot in competitive algorithm competitions
* Implementation
  * ![Img](../../../Images/Pasted%20Graphic%206%205.png)

## When to Use Decision Trees
* Decision trees
  * Works well on structured data: looks like a spreadsheet (features in a categorical fashion for ex)
  * Doesn't work well on unstructured data: images, audio, text
  * Fast to train so can improve quickly
  * Small decision trees can be human interpretable
* Neural networks
  * Works well on all types of data (structued, unstructured, mixed)
  * Slower, takes long time to train
  * Works with transfer learning because with small dataset, can just transfer learning many parameters
  * With many ML models working together, easier for multiple NNs vs multiple decision trees
* ![Img](../../../Images/Decision%20Trees%20vs%20Neural%20Networks.png)