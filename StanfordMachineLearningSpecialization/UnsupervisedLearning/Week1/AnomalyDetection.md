## Finding Unusual Events
* Looks at normal events so can detect when there is an anomaly
* Ex: For anomaly detection of a product. Measure some statistics like heat, force withstand, etc. for working product. Once algorithm has seen all examples and learns, test a new version and see if it looks similar to previous working product. If near to others, all good. If far away, then might have a problem
* Density estimation:
  * Given a training set, build a model for probability of being in dataset. Create circles around center that middle is high probability of being okay, then middle, then low
  * If probability is less than a threshold (unlikely to happen), then raise a flag to being an anomaly
* Uses:
  * Fraud detection to different user activities that might be fraudulent and done by another party. Instead of disabling their accont, maybe can ask to verify authentication again for the user

## Gaussian Distribution
* Aka normal distribution
* Probability is determined by mean and variance and is a complicated formula
* ![Img](../../../Images/Pasted%20Graphic%2013%204.png)
* With a dataset, can calculate the mu and sigma squared of the dataset
* Probability is low that something is on far of gaussian distribution and might be anomaly
* ![Img](../../../Images/Parameter%20estimation.png)

## Anomaly Detection Algorithm
* Density estimation:
  * In a training set, each example has n features
  * What is the probability of any feature vector? It is comprised of the multiplication of all the probabilities of the components (statistical independence not needed)
  * Different probabilities for each feature given different distributions for each feature. Then multiply them
  * ![Img](../../../Images/Pasted%20Graphic%2015%204.png)
* Steps:
  * Choose features and get training data
  * Fit the parameters to get the means and variances for each feature
  * Give a new example and compute the probabilities then multiply them
  * If the probability < epsilon (defined threshold), then it is an anomaly
  * ![Img](../../../Images/Pasted%20Graphic%2016%204.png)
* ![Img](../../../Images/Pasted%20Graphic%2017%203.png)

## Developing Evaluating Anomaly Detection System
* If you can quickly change a parameter value and can quickly check if better, it is easy to develop an algorithm
* ![Img](../../../Images/Pasted%20Graphic%2018%204.png)
* Again, want to break into training set, cross validation (cv), and test sets. Put the amount of data with the same ratio of good to bad into each set
* Don't need test set if have few labeled anomaly examples, but high risk for overfitting
* ![Img](../../../Images/Pasted%20Graphic%2019%204.png)
* ![Img](../../../Images/Pasted%20Graphic%2020%204.png)

## Anomaly Detection Vs. Supervised Learning
* When have labels, can use anomaly detection or supervised learning
* Anomaly:
  * When have small number of positive examples and large number of negative examples
  * Different types of anomalies. Where anomalies can look different than any anomalies seen so far
  * Ex: Fraud is different case everytime 
* Supervised:
  * Many number of both examples
  * Enough positive examples so that future are likely to be similar to ones in training set
  * Ex: Spam emails are likely to be similar to other spam emails used in the past
* ![Img](../../../Images/Pasted%20Graphic%2021%204.png)
* ![Img](../../../Images/Pasted%20Graphic%2022%204.png)

## Choosing What Features To Use
* In supervised learning, algorithm can see which features not relevant and just not use them. In unsupervised, more important for picking features because harder to see which features to use
* Make sure features are gaussian
  * We want it to look like a symmetric bell/normal curve. Can pick transformations that make it more gaussian
  * Can plot features as $x->log(x)$ to make more normal curve looking. Other transformations can do this
  * ![Img](../../../Images/Pasted%20Graphic%2023%203.png)
* Error analysis:
  * If doesn't work well on cv set, can see where the algorithm is not doing well
  * Can see an actual anomaly that isn't flagged and see why? Maybe there is a feature that I am not accounting for and can add that feature
  * ![Img](../../../Images/Pasted%20Graphic%2024%203.png)
* Can also do transformations of different features. Even feature transformations on other features
  * ![Img](../../../Images/Pasted%20Graphic%2025%204.png)