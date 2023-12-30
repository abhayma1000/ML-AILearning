## Error Metrics for Skewed Datasets
* Accuracy does not work well when lot's of negative results and not lot's of positives
* Some problems (like disease classification) have very little positives. Sometimes 1% error is not good because of problem
* ![Img](../../../Images/Pasted%20Graphic%2018%203.png)
* Precision/recall
  * Can construct confusion matrix. See how much classified right and wrong and which way
  * Can calculate the precision and recall to see how well model did on each way
  * ![Img](../../../Images/Pasted%20Graphic%2019%203.png)

## Tradeoff Between Precision Recall
* Sometimes ther eis trade off. Ex: For disease recognition, would rather have diagnosis false positive than false negative
* There is a bow curve that is the tradeoff between the two
* ![Img](../../../Images/Pasted%20Graphic%2020%203.png)
* Can combine precision and recall into one score w/ F1 score. F1 score better than average because it pays attention to which is lower
* ![Img](../../../Images/Pasted%20Graphic%2021%203.png)