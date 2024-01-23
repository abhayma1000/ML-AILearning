## What is Reinforcement Learning
* Ex:
  * Given position, how to control the vehicle
  * Function that goes from a state to an action
* Could use supervised learning where we get bunch of states and tell the algorithm what is the best move there, can make a NN for that
  * However, it is ambiguous what is the correct action to take and hard to get right
* Reward
  * Tells the vehicle when is doing well and when its doing poorly
  * Give say +100 when doing well and -1000 when it crashes and bad
* Applications
  * Controlling robots, optimizing factory operations, stock trading, and playing video games
* Not used as much as supervised learning, but instead of telling what is right, specify a reward function to tell when its doing well and when its doing poorly

## Mars Rover Problem
* Rover can be in any position out of 6. The position is called the state and each state is labeled
* State 1 is better, but state 6 is okay. This valuableness of state 1 is defined by a reward. In between there are no rewards so could go either way
* There is constantly some state, then an action, a new reward, and a new state again

## The Return in Reinforcement learning
* How you know one set of reward is better than another set. The return is what captures that
* Return is the sum of the rewards are for each state and weighted by the discount factor
  * Discount factor is picked and is <1 and is multiplied by each reward at each step
* ![Img](../../../Images/Pasted%20Graphic%201%208.png)
* Way of choosing which action to take based on location
* ![Img](../../../Images/Pasted%20Graphic%202%207.png)
* Rewards in the far future are reduced by discount factor

## Making Decisions
* Goal is to find a policy that to take what action at every state to maximize return
* ![Img](../../../Images/Pasted%20Graphic%203%2010.png)
* ![Img](../../../Images/Pasted%20Graphic%204%208.png)

## Review of Key Concepts
* States, actions, rewards, discount factor, return, and policy
* 6 states, actions to go in both directions, discount factor, return of the discount factor * rewards and a policy of where to go
* ![Img](../../../Images/Pasted%20Graphic%205%206.png)
* Called Markov Decision Process because the future depends on the current situation and the values associated
  * It is a loop where action leads to world, then state and reward leads back to the agent
  * ![Img](../../../Images/Pasted%20Graphic%206%207.png)