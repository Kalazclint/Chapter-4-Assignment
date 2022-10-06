1. What Linear Regression training algorithm can you use if you have a training set with millions of features?
Ans: Gradient decent is the machine learning algorithm you can use when there is millions of features

2. Suppose the features in your training set have very different scales. What algorithms might suffer from this, and how? What can you do about it?
  Ans: The Gradient Descent suffers from features of different scales, because the model will take a longer time to reach the global maximum.
  
3. Can Gradient Descent get stuck in a local minimum when training a Logistic Regression model? 
  Ans: Since Logistic Regression Model cost function is convex, there is no local minimum.

4. Do all Gradient Descent algorithms lead to the same model provided you let them run long enough?
  Ans: No. If the learning rate is too high, then the model can diverge. It can also only reach the local minimum based on where the initialization is.
 
5. Suppose you use Batch Gradient Descent and you plot the validation error at every epoch. If you notice that the validation error consistently goes up, what is likely going on? How can you fix this?
  Ans: If the validation error consistently goes up, It implies the model could be diverging because of high learning rate. If the training error also goes up, that is the indication of diverging. You can fix that by lowering the learning rate and then re-training. If the training error is not increasing, then your model is overfitting and you have to retrain with a different model.
  
 6. Is it a good idea to stop Mini-batch Gradient Descent immediately when the validation error goes up?
 Ans: No, because it will be erratic in approaching the minimum (just like Stochastic Gradient Descent, but to less degree). You can always revert to the best case if the error does not improve for a while.
 
 7. Which Gradient Descent Algorithm will reach the vicinity of the optimal solution the fastest? Which will actually converge? How can you make the others converge as well?
 Ans: The Stochastic Gradient Descent will reach the fastest since you are using one random training data at each iteration. However, the Batch Gradient Descent is the only one to actually converge. You cannot make the others converge; they will only approach close to the global minimum.
 8. Suppose you are using Polynomial Regression. You plot the learning curves and you notice that there is a large gap between the training error and the validation error. What is happening? What are three ways to solve this?
  Ans: The model is overfitting the data. To avoid overfitting the data, you can  regularize the model using Lasso or Ridge regression,or reduce the complexity of the model (degree of freedom)
9. Suppose you are using Ridge Regression and you notice that the training error and the validation error are almost equal and fairly high. Would you say that the model suffers from high bias or high variance? Should you increase the regularization hyperparameter alpha or reduce it?
  Ans: The model suffers from high bias, the is under fitting. To treat high bias, reduce the regularization hyper parameter
10. Why would you want to use:

- Ridge Regression instead of plain Linear Regression?

- Ridge Regression instead of plain Linear Regression?

    *Ridge Regression regularizes the Linear Regression, to avoid overfitting.*

  - Lasso instead of Ridge Regression?

    *Lasso, which uses L1 norm regularization, automatically eliminates the weights of the least important features and therefore performs feature selection.*

  - Elastic Net instead of Lasso?

    *Elastic Net is preferred over Lasso if there are lots of features or lots of strongly correlated features.*

11. Suppose you want to classify pictures as outdoor/indoor and daytime/nighttime. Should you implement two Logistic Regression classifier or one Softmax Regression classifier?

    Ans- You should implement two Logistic Regression classifiers, because there are two different binary classifying (outdoor vs indoor, daytime/nighttime). All pictures can be one from each classifier. Softmax Regression classifies into only one class out of all of them.*
