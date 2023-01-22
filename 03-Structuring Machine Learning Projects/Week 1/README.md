# ML Strategy (1)

**1. Learning Objectives**
- Explain why Machine Learning strategy is important
- Apply satisficing and optimizing metrics to set up your goal for ML projects
- Choose a correct train/dev/test split of your dataset
- Define human-level performance
- Use human-level performance to define key priorities in ML projects
- Take the correct ML Strategic decision based on observations of performances and dataset

**2. Introduction to ML Strategy**
**Why ML Strategy?**

You have a lot of ideas for how to improve the accuracy of your deep learning system:
- Collect more data
- Collect more diverse training set
- Train algorithm longer with gradient descent
- Try Adam instead of gradient descent
- Try bigger network
- Try smaller network
- Try dropout
- Add L2 regularization
- Change network architecture (activation functions, # of hidden  units etc.)

This course will give you some strategies to help analyze your problem and go in a direction that will help you get better results.

**Orthogonalization**

In the example of TV tuning knobs, orthogonalization refers to the fact that the TV designers designed the knobs so that each knob kind of does only one thing.  
In orthogonalization, you have some controls, but each control does a specific task and doesn't affect other controls.
For a supervised learning system to do well, you usually need to tune the knobs of your system to make sure that four things hold true—the chain of assumptions in machine learning:
|Chain of assumptions in ML |Tune the knobs  |
|--|--|
|Fit training set well on cost function (near human level performance if possible)  |If it's not achieved, you could try a bigger network or another optimization algorithm (like Adam). |
|Fit dev set well on cost function |If it's not achieved, you could try regularization or a bigger training set. |
|Fit test set well on cost function |If it's not achieved, you could try bigger dev set. |
|Performs well in real world |If it's not achieved, you could change dev set, cost function etc. (Either the dev test set distribution is not correct or the cost function not right) |

**Early stopping**, though not a bad technique, is a knob that simultaneously affects the training set and development set performance and therefore is less orthogonalized, so Andrew tends not to use it.

**3. Setting up your goal**

**4. Comparing to human level performance**
