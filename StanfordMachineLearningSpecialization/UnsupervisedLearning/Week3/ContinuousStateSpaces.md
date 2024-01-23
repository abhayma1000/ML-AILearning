## Example of Continuous State Space Applications
* Before we used that something can be one of discrete possible positions, however, can be on a continuous range of positions
* State might also have multiple numbers: x-pos, y-pos, angle/orientation, x-vel, y-val, anglular-vel
* ![Img](../../../Images/Pasted%20Graphic%2014%205.png)
* ![Img](../../../Images/Autonomous%20Helicopter.png)

## Lunar Lander
* A game famously used for reinforcement learning algorithms
* Four actions: nothing, left thruster, right thruster, main thruster. The state is kept in vector with positions and velocities
* ![Img](../../../Images/Pasted%20Graphic%2016%206.png)
* Rewards:
  * Rewards for soft landing, each leg grounded. Negative rewards to crashing and firing thrusters in general
  * ![Img](../../../Images/Pasted%20Graphic%2017%205.png)
* Given the states and rewards, take an action to maximize the rewards w/ a $\gamma$ close to 1

## Learning the State Value Function
* Train a neural network to approximate $Q(s,a)$
* NN architecture
  * inputs the current state + current action and gives Q(s,a)
  * Inputs the current state with a one-hot encoding of the actions
  * Try nn inputs with the different actions
  * Whichever action has a highest Q(s,a), pick that action
  * ![Img](../../../Images/Pasted%20Graphic%2018%206.png)
* Training
  * The bellamn equation is like the neural network
  * Use the bellman equation pairs each as different training examples
  * ![Img](../../../Images/Pasted%20Graphic%2019%206.png)
* Algorithm
  * Initialize NN with random guess of the Q(s,a) function
  * Repeatedly take actions in the playfield. Get tuples of state, action, reward, and a new state
  * Store recent examples of tuples
  * Now set the new Q function used to the one that has just been trained and repeat this
  * This improves so that the next model has better approximation of Q function, and so on and so on
  * ![Img](../../../Images/Pasted%20Graphic%2020%205.png)
* Called DQN (deep Q network)
* Can make refinements to make algorithm better

## Algorithm Refinement: Improved NN Architecture
* Architecture to make more efficient
* Difference:
  * Instead of running different times for different actions, can run all simultaneously. More efficient because run once instead of many times
  * The output layer instead of having one output, has four with different actions
  * ![Img](../../../Images/Pasted%20Graphic%2021%206.png)

## Algorithm Refinement: $\epsilon$-greedy Policy
* How to pick actions while still learning?
* Policy:
  * Previously, we have been picking the action that maximizes the Q function
  * Instead, with a high probability, we pick the action taht maximizes the Q function, but small fraction of the time, pick random action
  * Do this to make it learn new possibilities and be open to new actions
  * Called Exploration step. Regular maximizing Q(s,a) is called Greedy
* $\epsilon$-greedy policy is the name where $\epsilon$ is the probability that go random
* Trick is to start with high epsilon so taking lots of random moves initially, but over time to gradually decrease
* ![Img](../../../Images/Pasted%20Graphic%2022%206.png)
* Picking hyperparameters is more important in reinforcement learning than standard machine learning and can make things go much worse

## Algorithm Refinement: Mini-batch and Soft Updates
* Mini-batch speeds up algorithm. ALso works on supervised learning. Soft updates help algorithm converge earlier
* Mini-batch for Supervised
  * When we have a large dataset, you have to update the parameters according to the cost function over say 1mil examples and make a tiny step for the parameters. Very slow
  * Mini batch picks a smaller number m(prime) and instead of using all examples, use a subset of m for updating the parameters. Steps take less time
  * ![Img](../../../Images/Pasted%20Graphic%2045.png)
  * Might go noisily and wobble around, but in the end, takes must less time even though not perfect descent
  * ![Img](../../../Images/Pasted%20Graphic%201%209.png)
* Mini-batch for unsupervised
  * Instead of storing a lot of recent tuples, reduce that number, but cycle through
  * ![Img](../../../Images/Pasted%20Graphic%202%208.png)
  * Instead of updating Q everytime the same, have it weighted to be mostly the old W. Called soft update because only accept little of the new value of W
  * ![Img](../../../Images/Pasted%20Graphic%203%2011.png)

## The State of Reinforcement Learning
* Limitations
  * Research publications on simulated environments where simulations are easier to get an algorithm to work with than real world
  * Fewer applications compared to supervised+unsupervised learning
  * ![Img](../../../Images/Pasted%20Graphic%204%209.png)
