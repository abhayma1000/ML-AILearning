## State Action Value Function Def
* Function of a state and the action might choose to take there
* Gives the return at the state and taken the action a and assuming that performs perfectly after
* ![Img](../../../Images/Pasted%20Graphic%207%204.png)
* We want to maximize the Q function at the state. We go to the larger Q direction
* ![Img](../../../Images/Pasted%20Graphic%208%205.png)

## State Action Value Function Example
* See how the $Q(s,a)$ function will change depending on parameters
* Depending on the rewards, the optimal direction will change because the optimal rewards at each step changes
* ![Img](../../../Images/Pasted%20Graphic%209%205.png)

## Bellman Equation
* Go in the direction of maximum $Q(s,a)$, but how do we calculate that. Bellman equation helps calculate Q function
* Equation:
  * ![Img](../../../Images/Pasted%20Graphic%2010%206.png)
  * At the terminal state, $Q(s,a)=R(s)$
  * The Q is calculated in each direction at a certain state
  * ![Img](../../../Images/Pasted%20Graphic%2011%206.png)
* ![Img](../../../Images/Pasted%20Graphic%2012%206.png)

## Random Environment
* Sometimes, when we want a robot to go a certain way, it doesn't always follow. Might slip and has a chance of going wrong
* When there is randomness in the problem, we don't want to maximize reward, but maximize the AVERAGE of the returns so that even taking into account randomness, will still do well
* ![Img](../../../Images/Pasted%20Graphic%2013%206.png)
* Set the misstep probability that the actor will take a wrong step
