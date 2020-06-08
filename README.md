# cs643/Wine Prediction Using MLLib in Spark & AWS

The purpose of this individual assignment is to learn how to develop parallel machine learning (ML) applications 
in Amazon AWS cloud platform. Specifically, you will learn: 
(1) how to use Apache Spark to train an ML model in parallel on multiple EC2 instances; 
(2) how to use Spark’s MLlib to develop and use an ML model in the cloud



You have to build a wine quality prediction ML model in Spark over AWS. The model must be trained in parallel on multiple EC2 instances. Then, you need to save and load the model in an application that will perform wine quality prediction; this application will run on one EC2 instance. The assignment must be implemented in Java, Scala, or Python on Ubuntu Linux. The details of the assignment are presented below:
• Input for model training: we share 2 datasets with you for your ML model. Each row in a dataset is for one specific wine, and it contains some physical parameters of the wine as well as a quality score. Both datasets are available in Canvas, under Programming Assignment 2.
o TrainingDataset.csv:youwillusethisdatasettotrainthemodelinparallelonmultipleEC2 instances.
o ValidationDataset.csv: you will use this dataset to validate the model and optimize its performance (i.e., select the best values for the model parameters).
• Input for prediction testing: TestDataset.csv. We will use this file, which has a similar structure with the two datasets above, to test the functionality and performance of your prediction application. Your prediction application should take such a file as input. This file is not shared with you, but you can use the validation dataset to make sure your application works.
• Output: The output of your application will be a measure of the prediction performance, specifically the F1 score, which is available in MLlib.
• Model Implementation: You have to develop a Spark application that uses MLlib to train for wine quality prediction using the training dataset. You will use the validation dataset to check the performance of your trained model and to potentially tune your ML model parameters for best performance. You should start with a simple linear regression or logistic regression model from MLlib, but you can try multiple ML models to see which one leads to better performance. For classification models, you can use 10 classes (the wine scores are from 1 to 10). Note: there will be extra-credit for the top 5 applications/students in terms of prediction performance (see below under grading).

• The model training is done in parallel on 4 EC2 instances.
• The prediction with or without Docker is done on a single EC2 instance.
         
