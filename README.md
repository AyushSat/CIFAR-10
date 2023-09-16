# CIFAR-10 Trainer

It's common to use neural networks, specifically convolutional neural networks, are often used when it comes to computer vision. It makes sense why, but just what is the difference between using more fundamental classifiers like kNN or Decision Tree's to classify images? Let's find out.

In this project, I used different kinds of classifiers to test the differences between all the classifiers would be on the CIFAR-10 CV dataset. A good basis was given by [Mason Swafford](https://paperswithcode.com/paper/image-completion-on-cifar-10) who used a convolutional neural network to acheive an accuracy of 98.5%. Here, I tested different classifiers, including a K Nearest Neighbors Classifier, a LogisticRegression classifier, a Decision Tree Classifier, and a non convolutional Multi Layer Perceptron Neural Network.

Playing with the hyperparameters of each one allowed us to achieve the relatively best numbers we could get out of each classifier, given the computing power of a couple of laptops. 

The results were not too surprising:

Worst out of all was the Decision Tree classifier, with the best accuracy at **27.89%**. Then, not too far forward was kNN, at **31.98%**. Second best was LogisticRegression, at **35.82%**, and best of all was the neural network at **44.22%**. 

In a separate project, I manually created each of the algorithms from scratch, and stepping through the data revealed why the numbers were inaccurate.

Decision tree's primarily operate by splitting data recursively, kNN operates by finding the closest classified data to the test data, and logisitic regression operates by transforming binary values into percentages. The main issue with all of these, even neural networks, is that they all are almost "assuming" that an object would be in the same place. Convolutional neural networks recursively scan smaller and smaller grids to almost hone in on objects, allowing the accuracy to jump so much higher.
