## Decision Tree Model
* Widely used decision trees and ensembles, but has not recieved much recognition in academia
* Features are categorical values
* ![Img](../../../Images/Pasted%20Graphic%2022%203.png)
* Main nodes of a tree and looks at new example will look at top node (root node). Then follow down node into which classification
  * ![Img](../../../Images/Pasted%20Graphic%2023%202.png)
* Different decision trees you can make for a problem. Some do better, some worse
* ![Img](../../../Images/Decision%20Tree.png)


## Learning Process
* How to build a decision tree
* ![Img](../../../Images/Pasted%20Graphic%2025%203.png)
* Given a training set, decide what features to use at root node to split on.
* Decisions:
  * How do we choose which feature to split on at the node? We want to maximimize purity
    * Later will see how to maximize purity
  * When do we stop splitting? Either when node is 100% one class (or to some specified percentage). When splitting will result in the tree exceeding max depth. Might want to limit the depth so it is not too unwieldy and less prone to overfitting. Also done when splitting a node has minimum improvements, then not worth it
  * ![Img](../../../Images/Pasted%20Graphic%2026%202.png)
  * So many ways to determine whether to stop splitting coming from years of research
