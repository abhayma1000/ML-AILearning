## Collaborative vs. Content Based
* Collaborative recommends based on ratings of users similar to you
* Content recommends items based on features of user and features of the items that match (features of users and features of items)
* ![Img](../../../Images/Pasted%20Graphic%2011%205.png)
* Is a given movie vector a good match for a user vector? They are of different sizes
  * ![Img](../../../Images/Pasted%20Graphic%2012%205.png)
* Take dot product between the two vectors to find a good match
* ![Img](../../../Images/Pasted%20Graphic%2013%205.png)

## DL for Content Based Filtering
* Architecture:
  * Need Neural Networks to translate the feature vector to the output vector for both the user vector and the item vector
  * one NN for each side. Each output layer has many units, but same on each side
  * Final prediction: $v_u * v_m$
  * ![Img](../../../Images/Pasted%20Graphic%2014%204.png)
* Training
  * In order to train both NNs, sum over all examples and find difference between prediction with the rating
  * ![Img](../../../Images/Pasted%20Graphic%2015%205.png)
* ![Img](../../../Images/Pasted%20Graphic%2016%205.png)

## Recommending From a Large Catalogue
* Have a large catalogue of items to choose from. How to choose from vast catalogue and how to put all those items in nn? Not computationally feasable
  * ![Img](../../../Images/Pasted%20Graphic%2017%204.png)
* Retrieval step
  * Generate list of plausable candidates
  * Maybe: For last 10 movies watched, find 10 similar movies to retrieve. Can be pre-computed so easy to pull up. Gives set of plausable things to reccomend
  * Maybe: Then see the most viewed genre and pick the top 10 movies from those gengres
  * Basically pick a system to retrieve likely recommended items
  * ![Img](../../../Images/Pasted%20Graphic%2018%205.png)
* Ranking step
  * Find the best item out of retrieval step list
  * Take the list and rank them based on learned model
  * ![Img](../../../Images/Pasted%20Graphic%2019%205.png)
* Can retrieve more results, gives better recommendation, but slower
* ![Img](../../../Images/Pasted%20Graphic%2021%205.png)

## Ethical User of Recommender Systems
* Different goals of recommender systems and not always in best interest of user, but instead the producer (company)
* ![Img](../../../Images/Pasted%20Graphic%2022%205.png)
* Different industries have different incentives which sometimes align with customer interests and sometimes do not
* ![Img](../../../Images/Pasted%20Graphic%2023%204.png)
* ![Img](../../../Images/Pasted%20Graphic%2024%204.png)

## Tensorflow Implementation
* ![Img](../../../Images/Pasted%20Graphic%2025%205.png)
* Similar implementation to normal, but make a dot product layer in the end through keras
