## Linear Regression Model
* Fit a line to the data and use it to interpolate value for new data point
* Terminology:
  * Data set: The data used to train the model
  * x: input variable/input feature
  * y: target variable
  * m = number of training examples
  * $(x^{i},y^{i})$ = single training example
* Model:
  * Training set --> Learning algorithm --> Function/Model --> y-hat (estimate)
  * In linear regression, $f(x) = wx+b$

## Cost Function
* Tells us how well the model is doing so we can get it to do better
* In the model, w and b are parameters and are coefficients that can be changed: $f(x) = wx+b$
  * w is the slope, b is the y-int
* Cost function takes in predicted value (yhat) and finds how far off from actual y
  * Takes difference $J(w,b) = (1/2m)*\sum_{i=1}^m(yhat-y)^2$
    * ^^This the squared error cost function. Used a lot for linear regression
  * ![Img](../../../Images/Screenshot%202023-11-14%20at%208.31.03%E2%80%AFPM.png)


## Cost Function Intuition
* Goal is to minimize $J(w,b)$ therefore change w,b to minimize the function
  * At the correct w,b values, $yhat - y = 0$ therefore working to minimize the cost function
  * The minimizing function is a Function w by J(w). Try to find lowest point in graph
    * ![Img](../../../Images/Screenshot%202023-11-14%20at%2010.30.06%E2%80%AFPM.png)
* Multi-dim cost function
  * With multiple parameters like w and b, then there is 3d plot with J(w,b) where we try to minimize the 3D function
  * Visualizations:
    * Can use a contour plot to visualize or a 3D plot
    * 