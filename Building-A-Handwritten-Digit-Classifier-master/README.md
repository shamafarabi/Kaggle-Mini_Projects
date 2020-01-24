 # Building-A-Handwritten-Digit-Classifier
This repository contains the code for classifying images of handwritten digits using different machine learning and Neural Network models. The idea behind this project was to understand how to implement image classification in machine learning while exploring the advantages and limitations of different conventional and neural network models. 

# Solution Approach
Using  a dataset of images available from sklearn.datasets, classification is first performed with a conventional approach such as K Nearest Neighbors. During this step, modeling was attempted with different values of K(i.e. number of nearest neighbors) to check how tuning this parameter affects the prediction accuracy by the model. We chose the k-nearest neighbors algorithm over linear and logistic regression models as both make assumptions about the linearity between the features and the output labels. As KNN makes no such assumption, this should allow them to capture any nonlinearity in the data. 

Next, classification of the images with neural network model is implemented while demonstrating the effect of tuning some of the modeling parameters  on prediction accuracy. (e.g. the number of neurons in a hidden layer using single and the number of hidden layers in the model). 

As all the accuracies were calculated by using 4fold cross validation to test the performance of the model on unseen data, the scores should give us a fair idea if any of these models are likely to overfit. 

# Summary
* Classifying with KNN has a maximum accuracy of 96.7% and it decreases with k (i.e. number of nearest neighbors). However, for all the values of K considered, the model provides more accuracy (~88.5%) than a neural network model that has only  8 neurons in a single hidden layer. 
* As the number of neurons in the hidden layer is increased,  the accuracy of the neural network approach is significantly improved up-to ~ 94.6% for a single layer with 256  neurons. 
* Repeating the neural network approach with two and three hidden layer shows that further improvement in the accuracy is possible by adding more hidden layers in the network. For example, when number of layers is increased from one to three with 64 neurons in each layer, the accuracy is improved from 93.4%  to 94.9%.

# Future Work
While the project showed that the accuracy of prediction by neural network model can be improved by incorporating more neurons and hidden layers in the model, further improvement of the classification model is possible by finding an optimized combination of neurons, hidden layers and other parameters (e.g. activation function). While neural network is known to be a better alternative of traditional Machine Learning models such as KNN or Random Forest, KNN gave the best accuracy for the modeling parameters explored for each model in this project. Future work on this project can be performing a hyper-parameter optimization using available packages such as GridSearchCV or RandomSearchCV and then comparing all the models in terms of their best prediction score.

# Files in the Repository
* *HandWrittenDigitClassifier.ipynb* contains the code written in a Jupyter Notebook for Python 3. <br>
* *requirements.txt* contains a list of all the packages used in the project.

# Installation
* Install the requirements using pip install -r requirements.txt.
* Make sure you use Python 3


