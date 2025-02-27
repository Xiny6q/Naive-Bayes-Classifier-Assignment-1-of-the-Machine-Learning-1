Download link :https://programming.engineering/product/naive-bayes-classifier-assignment-1-of-the-machine-learning-1/

# Naive-Bayes-Classifier-Assignment-1-of-the-Machine-Learning-1
Naive Bayes Classifier Assignment 1 of the Machine Learning 1
1 Introduction

In this article, we will discuss the classification problem, in par-ticular with the Naive Bayes Classifier.

In classification we have an object, called classifier, that asso-ciates each input with an output (also called class). In order to classify correctly the inputs, the classifier needs to study a set of inputs along with their respective classes. With the training process, the classifier acquires the knowledge to assign the new input to the corresponding classes.

There are many different types of classifiers, but the simplest, still efficient, is the so-called Naive Bayes Classifier, which is a statistical classification technique based on the Bayes Theo-rem.

where vk is the possible value for the attribute k.

2.1 Improvements with Laplace Smoothing

If we use a small data set we may encounter a problem, some combinations that appear in the test set may not be encoun-tered in the training set, so these probabilities will be zero. This causes a big problem since just one zero will cause the overall results to be zero.

The Laplace Smoothing takes into account those attributes that could not appear in the training set but are present in the over-all data set, it introduces a trust factor (α) in the conditioned probability computation such that is will never be equal to zero, even if some values do not appear in the training set.



Figure 1. Wheather dataset

3.1 Data pre-processing

In machine learning datasets are usually provided in csv format. All values of the data set are categorical, so they need to be converted into numerical values, afterward, I split the data set into a test set and a training set, respectively 30% and 70% of the data set. I also separated the target column from the dataset. To be sure that the split was successful I performed a check that the test and train matrices have the correct dimensions.

3.2 Build the Naive Bayes Classifier

The naive Bayes classifier is implemented as a class with two methods:

a fit method that takes care of the training session;

a predict method that makes the classification of the pre-dicted classes;

the error method that computes the error rate of the pre-diction.

In particular, the fit method calculates the prior and the condi-tional probabilities for each feature, which will then be used by the predict method to compute the posterior probabilities.

Finally the predict method returns the predicted classes that will then be printed on the console.

The error method takes care of computing the error rate, which is computed as the number of wrong predictions divided by the number of total observations.

3.3 Improve the classifier with Laplace smoothing

We take an α factor of 1 defined as a global constant for the Laplace smoothing. Then the classifier is pretty much the same as before, we just have to add the α factor to the conditional probabilities calculation.

4 Results

When we run the program, it will print in the console three parameters: the actual values of the classes, the result of our prediction, and the error rate. An example of a possible output is shown in the following figures:

Figure 2. Prediction results (50% error rate)



Figure 3. Prediction results (25% error rate)
