## What is Clustering
* Looks at data points and finds those that are related/similar
* In unsupervised learning, given just data (no output y)
  * Since we don't have and y's, cannot predict. Instead, algorithm finds interesting structure in data
  * Clustering looks for structure and tries to group points into clusters
  * ![Img](../../../Images/Pasted%20Graphic%208%203.png)
* Applications:
  * Group similar news together
  * Market segmentation of different users of a platform
  * Similar astronomical objects

## K-means Intutiion
* First, tell it how many clusters to find. Pick random points where the centers of the clusters may be
* Assign each point to closest center
* Recompute the average of the points of each center and assign to be the new center
* Repeat this process until the center now contains a good group (converged) and no further changes can be made
* ![Img](../../../Images/Pasted%20Graphic%209%203.png)
* ![Img](../../../Images/Pasted%20Graphic%2010%204.png)

## K-means Algorithm
* Steps:
  * Randomly instantiate the center for k number of groups wanted
    * n=number of features per example and k=number of groups wanted
  * Assign points to each cluster center. Pick the center that minimizes the squared distance between center and point
  * Move cluster center to mean of points assigned to the cluster
  * Repeat setps
  * Case: A cluster has zero points. Then just eliminate that cluster so have k - 1 clusters
  * ![Img](../../../Images/Pasted%20Graphic%2011%204.png)
* Not well seperated clusters:
  * Ex: If have size and weight of clients. Can split into three groups for small, medium, large t-shirts to make different sized shirts that will fit clients
    * Even if not well sepeated, gives three distinct groups that can now use
  * ![Img](../../../Images/Pasted%20Graphic%2012%204.png)

## Optimization Objective
* K means algorithm is an optimization problem but the algorithm (as shown earlier) is different from gradient descent
* Cost function: Average of the squared distance between each training example and the center
* Optimization algoirthm:
  * Minimizes the cost function
  * In order to minimize the cost, assign the examples to the closest centroid, thus minimizing it
  * The cost function should always go down (or plateau). If the centrers stay the same (or move less than a threshold), the algorithm has converged

## Initializing K-means
* First step is to choose random locations for cluster centers
* Random initialization:
  * Pick K training examples and set the centers to the average 
  * Can run into local minima for optimization depending on how it is initialized
* Can run multiple times and try to run best minima of the cost function. Take the lowest cost function
* Process:
  * For 100 times,
  * Randomly initialize means
  * Run algorithm
  * Compute cost function
  * Compare cost function for all 100 times and choose the set of clusters w/ lowest cost, often good choice

## Choosing the Number of Clusters (K)
* Clustering is subjective. Can have multiple right answers, so no correct number of clusters
* Elbow method:
  * Run the algorithm and cost cost function as function of number of clusters (k)
  * Find point (elbow) where cost function starts to level off and not decrease as much
  * Not the best algorithm b/c not always have an elbow
* Better choosing method:
  * Evaluate the value of K in the larger problem context and evaluate on how well it does in its purpose
  * Ex: T-shirt sizes can pick s,m,l with k=3 clusters because it makes sense