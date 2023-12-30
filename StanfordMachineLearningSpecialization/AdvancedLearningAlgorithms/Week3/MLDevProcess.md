## Iterative Loop of ML Dev
* Steps
  * First decide the overall architecture of the model
  * Then, implement and train the model
  * Almost never works the first time, so take diagnostics
  * Then, make changes to the architecture and the loop continues
  * ![Img](../../../Images/Pasted%20Graphic%205%204.png)
* Example project
  * Spam classifier:
  * Take the top words and make into 10,000 input features
    * Or can have new words and count how much each word is used. Like a spam might say the word buy multiple times
  * ![Img](../../../Images/Pasted%20Graphic%206%204.png)
  * Build it
    * Can collect more data
    * Can make sophisticated features from the words. Ex: compress words that are synonyms to one meaning or detect misspellings


## Error Analysis
* Manually looking through the misslassified cv set or test set and classify them based on common traits
  * Find how many of certain characteristics. Prioritize the most common (highest # occurances)
  * Pick a relatively medium size of examples to pick that it misslassifies. Sample a random subset. Don't have infinite time to look at
  * Maybe need new features, more data, etc. based on error analysis
* Note: Error analysis is hard to do for tasks that humans are not good at because we might not know what is wrong with the model because we are not experts at that topic ourselves
* ![Img](../../../Images/Pasted%20Graphic%209%202.png)


## Adding Data
* Sometimes tempting to get more data for everything. Instead, add more data where error analysis says we should get it
  * Maybe have a pot of unlabeled data so can go through that and find the data you need help on
  * ![Img](../../../Images/Pasted%20Graphic%2010%203.png)
* Data augmentation
  * Can create new training examples by distorting img, rotating it, and doing other operations
  * Distorsions to the data should be representative of what will happen in the real world
  * ![Img](../../../Images/Pasted%20Graphic%2011%203.png)
  * Can introduce random warpings too
    * ![Img](../../../Images/Pasted%20Graphic%2012%203.png)
  * For speech recognition, can add noisy background filter + bad cellphone, etc. to make the algorithm better
* Model centric approach is changing model, # neurons, layers, etc. Data centric approach is getting new examples, engineering data. Data centric becoming more popular


## Transfer Learning
* Uses data from another task where you don't have a lot of data. Used frequently
* Workings:
  * For image regression, say want to recognize certain classes. Have dataset for different recognition problem
  * Change the output units to what your problem is
  * Need new parameters for the output layer, and leading to that. Use the parameters from the first few layers of the original problem and transfer that over
  * Train on your limited data to refine the first few layers and then train the last layer. Called fine tuning
  * ![Img](../../../Images/Pasted%20Graphic%2013%203.png)
* Called transfer learning because although learned on different dataset, the first few layers learn some common aspects between the two problems and then switch over
* People will post their pre-trained networks on the internet to use for transfer learning. Then replace the output layer and it's good
* Why does it work (computer vision):
  * First layer detects edges, next layer groups those together to make corners
  * Learns generic features that are useful for other cv problems
  * Downside: Input size has to be the same size image
  * ![Img](../../../Images/Pasted%20Graphic%2014%203.png)
* Summary:
  * Lot's of sharing in the ML community to help everyone
  * ![Img](../../../Images/Pasted%20Graphic%2015%203.png)

## Full Cycle of ML Project
* Training model is just small part of it
* Cycle:
  * Scope out and define the project
  * Define what data and then collect the data
  * After initial data collection, train the model
    * Carry out error analysis with iterative improvement to the model
    * Might realize need to collect more data or certain types of data
  * Deploy to production. Monitor the performance and maintain the system to keep performance good
    * Maybe get data from the production to further help the model
  * ![Img](../../../Images/Pasted%20Graphic%2016%203.png)
* Deploying
  * Deploy the model in a server where it can be called upon by say a phone app API call and return a prediction
  * Need different software engineering skills to implement this client server model
  * Need to fix models when new data comes in. Ex: New president gets elected and is searched up a lot. Retrain the model and update the model -> deploy
  * Growing field ML-Ops how to deploy/maintain ML deployments
  * ![Img](../../../Images/Pasted%20Graphic%2017%202.png)


## Fiarness, Bias, and Ethics
* Should be fair and take an ethical approach
* Bias:
  * Can discriminate against races, genders, etc.
* Adverse use cases
  * Can generate fake videos like deep fakes
  * Can generate fake content and spread toxic speech
  * Spam. But also anti-spam which is countering this
* Wish there was a checklist for ethics, but hard to do for AI. It is a case by case basis
* Guidelines:
  * Get a diverse team and generate how possible harm to different groups
  * Carry out search and guidelines for the industry
  * Audit before deployment to see if any ethical wrongdoings. Then develop mitigation plan after deployment to prevent future harm 