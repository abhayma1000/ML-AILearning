## What is ML
* Study that gives ability to learn without being explicitely told
* After playing lot's of games/training a lot, able to get better

## ML Algorithms
* Main two are supervised and unsupervised learning. Other two are recommender systems and reinforcement learning
* Supervised is used most and has most real-world applications

## Using
* Need to know practical ML b/c going in the wrong direction can cost lot's of time and money

## Supervised Learning
* Maps x-->y or input-->output
* Give algorithm the right answers to learn from and eventually learns to take in just x and predict y
* Ex:
  * Email-->Spam?(y/n)
  * Audio-->Text transcript
  * English-->Spanish
  * Ad,user info-->Click?(y/n)
* Regression
  * Can plot data on x/y plane. Can make line and use to predict y
  * Can instead plot a curve that might be more accurate
* Classification
  * Ex: Detection of disease (y/n). Or multiple diff types of diseases too
  * Different than regression because guessing from a set number of outputs. Regression guesses from an infinite number of possible outputs
  * Can have multiple different outputs and multiple inputs (multi-dim) to map to those outputs (categories)

## Unsupervised Learning
* Not given labels or anything. Just find some pattern or something interesting in the data
* There is no right answer, just find patterns based on similar characteristics
* Types:
  * Clustering
  * Anomaly detection: Find unusual points
  * Dimensionality reduction: Reducing big dataset to smaller set w/o losing much info
* Ex:
  * Finding two groups/clusters within the data
  * Google News where groups different related stories together
  * In a DNA table with different people and traits, can group people together based on characteristics, but not knowing the groups
  * Grouping customers into different groups to cater specific products


## Jupyter Notebook
* Test environment to do oconcepts
* Being used by big companies
* Layout
  * Markdown text cell
  * Code cell which can run
  * 