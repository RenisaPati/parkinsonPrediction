# parkinsonPrediction

Parkinson’s disease is a nervous system disorder that affects a person’s mobility eventually. There are many symptoms that can show up few years prior to the person acquiring the disease. Some of these symptoms include shaking, slowed movement, rigidity, dementia and depression. In a 2017 survey it was observed that more than 10 million people worldwide are living with PD.
This project is an attempt to create a precise predictor for predicting the likelihood of a person acquiring said disease. We shall be using a dataset that was created at the University of Oxford, in collaboration with 10 medical centres around the US, along with Intel who developed the device used to record the primary features of the dataset: speech signals. 

Workflow
I shall be proceeding in the following way with this project:
1. Data cleansing: Data shall be processed for detecting and correcting corrupt or inaccurate records if any!
2. Manual feature reduction: Before even loading the data I shall try reducing the features. Such as eliminating IDs, Names, Sequence Numbers etc.
3. Data loading: Data shall then be converted from CSV to Panda’s DF format for carrying out further operations. This can be done using pythons Pandas library.
4. Train-Test split: The data shall then be split into an 80:20 ratio for carrying out ML classification on the training set.
5. Classifier show down: I shall use Python’s SciKit-Learn library for running all the classifiers in a loop  and figuring out the score for the most accurate classifier.
6. Feature reduction: Following the showdown the features shall be reduced using various techniques such as PCA to enhance the accuracy of the model.
7. Selecting best classifier: I shall then test the fit with reduced dimensionality with the classifiers which seemed to perform well during initial classifier showdown.
8. Fine tune: Finally the classifier parameters shall be tuned to increase classifier accuracy.
9. Prepare final model: This classifier shall then be used to prepare the final model.

It was observed that Support Vector Classifier outperformed all the other classifiers by a 5% margin. After tuning the number of PCA component between 4-15 and performing exhaustive gridSVC an accuracy of 90% was obtained with given parameters.

Further the following readings obtained from the confusion matrix emphasised on the fact that SVC fit our model the best out of all other classifiers.
Average Precision: 0.91
Recall: 0.90
f1-Score: 0.88

Future Work:
The model proposed in this project is restricted strictly to machine learning classifiers without the usage of neural networks due to the lack of sheer computing power. With enough resources, i.e A machine with a decent GPU, neural networks could be used to rebuild the classifier. 

Using a fine tuned neural network would lead to considerable gains in accuracy of the model.We could also collect more sample of data and retrain the model based on this data.Advantages of neural networks include their high tolerance to noisy data, as well as their ability to classify patterns on which they have not been trained

Other than enhancing the model using different methods, we can embed the current model into an application such as healthcare diagnostic systems to help in identifying patients who have a likelihood of acquiring parkinson's in the near future.
