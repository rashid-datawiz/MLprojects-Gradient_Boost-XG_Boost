# MLprojects-Gradient_Boost-XG_Boost

## What is GB and XGB ?
* XGBoost is a decision-tree-based ensemble Machine Learning algorithm that uses a gradient boosting framework. A wide range of applications: Can be used to solve regression, classification



* XGBoost is an implementation of gradient boosted decision trees designed for speed and performance



* Boosting is an ensemble technique where new models are added to correct the errors made by existing models. Models are added sequentially until no further improvements can be made.



* Gradient boosting is an approach where new models are created that predict the residuals or errors of prior models and then added together to make the final prediction. It is called gradient boosting because it uses a gradient descent algorithm to minimize the loss when adding new models.



* This approach supports both regression and classification predictive modeling problems.


**Why does XGBoost perform so well?**
* XGBoost and Gradient Boosting Machines  are both ensemble tree methods that apply the principle of boosting weak           learners using the gradient descent architecture. However, XGBoost improves upon the base GBM frameworkthrough systems optimization and algorithmic enhancements.


#### 1.Regularization: 
* This is considered to be as a dominant factor of the algorithm. Regularization is a technique that is used to get rid of overfitting of the model. 

#### 2.Cross-Validation: 
* We use cross-validation by importing the function from sklearn but XGboost is enabled with inbuilt CV function.

#### 3.Missing Value:  
* It is designed in such a way that it can handle missing values. It finds out the trends in the missing values and apprehends them.

#### 4.Flexibility:
* It gives the support to objective functions. They are the function used to evaluate the performance of the model and also it can handle the user-defined validation metrics.



## System Optimization

#### Parallelization:
* XGBoost approaches the process of sequential tree building using parallelized implementation. This is possible due to the interchangeable nature of loops used for building base learners; the outer loop that enumerates the leaf nodes of a tree, and the second inner loop that calculates the features. This nesting of loops limits parallelization because without completing the inner loop (more computationally demanding of the two), the outer loop cannot be started. Therefore, to improve run time, the order of loops is interchanged using initialization through a global scan of all instances and sorting using parallel threads. This switch improves algorithmic performance by offsetting any parallelization overheads in computation.

#### Tree Pruning: 
* The stopping criterion for tree splitting within GBM framework is greedy in nature and depends on the negative loss criterion at the point of split. XGBoost uses ‘max_depth’ parameter as specified instead of criterion first, and starts pruning trees backward. This ‘depth-first’ approach improves computational performance significantly.


#### Hardware Optimization:
* This algorithm has been designed to make efficient use of hardware resources. This is accomplished by cache awareness by allocating internal buffers in each thread to store gradient statistics. Further enhancements such as ‘out-of-core’ computing optimize available disk space while handling big data-frames that do not fit into memory.









**When to Use XGBoost?**

* 1> When you have large number of observations in training data.**

* 2> Number features < number of observations in training data.**

* 3> It performs well when data has mixture numerical and categorical features or just numeric features.**

* 4> When the model performance metrics are to be considered.**
