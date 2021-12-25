# ACN
Practical and Conﬁgurable Network Traﬃc Classiﬁcation Using Probabilistic Machine Learning

ACKNOWLEDGEMENT 

This report took a lot of time, effort, and attention to complete. Nonetheless, it would not have been possible without Prof. Raj K Jaiswal of the Department of Computer Science and Information Systems' help and continual mentoring. He gave us all  the needful information and input we needed to properly complete this project. As a result, we'd like to express our heartfelt gratitude to him.
I also thank my parents for the unceasing encouragement, support, and attention and listened to all my problems even when they can do nothing of it but listened to all problems and had provided mental support which eventually played a big role.
Furthermore, I am thankful and fortunate enough to work under the guidance of Dr. Raj K Jaiswal for all the knowledge they have imparted, which I could put to use in this project.
Most importantly, last but not the least, I appreciate the co-operation and benevolence of my friends for helping me with the data recording and my family for cheering me up all throughout this journey.
This project required a lot of dedication and hard work from our team members so we would like to appreciate the combined effort of our team.
 
 
KEYWORDS

Random forest, 
Probabilistic Random Forest, 
Feature selection, 
Confusion Matrix, 
Classification. 











ABSTRACT

In today’s world, a lot of systems (be it online or offline) employ machine learning (ML), with the rapid expansion in the storage capacity and processing power of computers, the machine learning area, which may be succinctly defined as enabling computers to make effective predictions based on past experiences, has seen spectacular growth recently. Machine learning approaches have been widely used in bioinformatics, as well as many other areas.
Many network security and management tasks require network traffic classification that is both widely applicable and highly accurate. It's best to employ a flexible and easily configurable classification framework that can be adapted for use in a range of networks. In this research, we offer a highly configurable and flexible machine learning traffic classification system that distinguishes known, or approved, traffic from unknown traffic using just statistics of packet sequences.
Thus, with the introduction of Probabilistic algorithms, we tried to improve the likelihood estimation provides a measure of certainty for classiﬁcation decisions, here given a network we try to predict classes of packets that flows in a particular network.




















 INTRODUCTION

Eﬀective and practical classiﬁcation of network traﬃc is crucial to many network management and security tasks because the extent and complexity of the Internet continue to grow much faster than our ability to characterize, understand, control, or predict it. There are numerous papers in the subject of Internet traffic classification study that represent various attempts to classify whatever traffic samples a researcher has access to, with no systematic integration of results. Categorization of network traﬃc yields valuable information about the flow of traffic in that network which can also help us in identifying various properties, as well as security of the network, could be analyzed.
 
We had divided traffic into two categories: known and unknown. The known class contains traffic from a set of applications that have been allowed for network use, while the unknown class contains traffic from any application that is not in the recognized group. These class definitions are well-suited to real-world networks such as the Science DMZ, and they take advantage of the fact that networks with specific intended application usage typically allow apps with similar functions and behaviours. Because the unknown class's broad definition permits it to encompass a wide range of application traffic, the difference between unknown and known traffic is bound to be greater than the variation within the known traffic class. The recognized class will often comprise applications with similar functions and traffic, whereas the unknown class will contain a wide range of applications with varying functions and traffic behavior based on previously observed traffic Our machine learning algorithm successfully finds and uses these differences for classification. This class system is also flexible because the known class can be defined with any set of applications, allowing network administrators to create a bespoke known class for their network with applications that are permitted to be used on it. As a result, our technique can be easily customized to meet a wide range of network requirements and is extensively relevant to various real-world networks. The following are the main contributions made by this work: 
 
Tested Outcomes
 
We showed a probabilistic machine learning approach for accurately classifying traffic. We show how the certainty of classification decisions may be simply tweaked to produce different outcomes. 
 
 
 
 
 
 
LITERATURE SURVEY
Existing Work
	
For traffic classification, a variety of machine learning techniques have been used. Traditional supervised learning approaches for classifying traffic into predefined classes, such as decision trees and Bayesian analytic techniques, were applied in earlier research. 
On a variety of applications, these methods have been demonstrated to execute classification with an accuracy of above 95%. Unsupervised and semi-supervised learning methods have also been investigated, where traffic is categorized based on similarity rather than being explicitly classified into a class. Deep learning has been applied in recent methodologies, with convolutional neural networks and recurrent neural networks doing supervised classification. Other neural network approaches, such as auto-encoders and generative adversarial neural networks, have employed unsupervised learning to learn traffic representations as well as how to simulate traffic.

Classification Schemes

The majority of present research focuses on categorizing traffic by allocating it to a specific application, application category, or protocol. A few classify traffic into known and unknown classifications by identifying a certain, known application or collection of apps from other traffic.
In our work, we employ the Probabilistic Random Forest Method which will estimate the likelihood of class flow in network 
We had used statistical and probabilistic methods such as naïve bayes, Probabilistic Random Forest etc. to improve prediction accuracy and can get better security against an attack.






 
 
 
BACKGROUND
Probabilistic Random Forest

Key Feature
Rather than treating features and labels as deterministic quantities, the Probabilistic Random Forest (PRF) approach treats them as probability distribution functions. We run a series of experiments in which we inject various types of noise into a data set and compare the PRF's accuracy to that of the RF. With a small increase in running time, the PRF outperforms the RF in all circumstances.


Mathematical Background
The PRF method, which we offer here, is an RF-based classification system that aims to improve the classic RF's prediction capabilities. This is accomplished by taking into account unknowns in the input data and making use of the information contained therein In terms of qualitative data, RF receives a sample of randomly selected observations pairs,
(x1,y1), (x2,y2) …. (xn,yn)
There is some relation which is modeled and then used to a degree of confidence h: X -> Y.
PRF, on the other hand, predicts y for a given value of x from a quadruplet sample,
(x1,y1,Δx1,Δy1), (x2,y2,Δx2,Δy2) …. (xn,yn,Δxn,Δyn)
where Δxk and Δyk denote the degree of uncertainty in the situation measurements. The PRF will predict (x,Δx), Taking into account the precision of each measurement.










Visual Comparision of Random Forest And Probabilistic Random Forest






State Description of Random Forest as well as Probabilistic Random Forest


PROPOSED MODEL



Here we have taken NSS-KDD dataset for training classification model to predict network classes process is as follows:
Dataset Preprocessing 
Feature Selection
Training Model
Logistic Regression
Gaussian Naive Bayes
Random Forest
Probabilistic Random Forest
Choosing Best Model based on Accuracy
 
Dataset Preprocessing 
Standard Scaler:
It standardizes features by subtracting the mean value from the feature and then dividing the result by feature standard deviation. So we get zero mean unit variance.
So first we have extracted all the continuos data columns and then applied Standard Scaling on that columns.
Random Sampling:
As the data was imbalanced we had generated equal distribution dataset using Random Sampling.
 
Feature Selection
We have used Random Forest and Probabilistic Random Forest on our training dataset and found out which features are more important and which we can neglect in order to get better results as well as better time complexity.
 
Random Forest(RF)
 
 
 
 
		Probabilistic Random Forest(PRF)
 
		
		Difference Between Feature Selection of RF and PRF
 
Here we can observe that the RF graph is more right-skewed, in comparison to the PRF graph, this clearly shows that RF has a high dependency on a few of the features whereas it neglects the remaining one whereas PRF model provides us maximum possible equal distribution among features in the dataset
Therefore clearly we can expect high accuracy from PRF model.
 
Training Models
After preprocessing the dataset we will train that dataset on our four models which are
Random Forest
Probabilistic Random Forest
Gaussian Naive Bayes
Logistic Regression
Here we have used 2 probabilistic models which are Probabilistic Random Forest and Gaussian Naive Bayes
Whereas we have used 2 classification models as well which are Random Forest and Logistic Regression
Choosing Best Model based on Accuracy
Hereafter training all the models Probabilistic Random Forest is the one that gave us maximum accuracy.
 
 
Proof of why we got such high accuracy with probabilistic Random Forest
Probabilistic Random Forest outperforms Logistic Regression, Random Forest and Naïve Bayes because it treats every feature as distribution instead of taking deterministic value so checks deviation in a feature by adding noise to data for some specific iteration thus we can get better performance from Probabilistic Random Forest as it considers distribution among the values rather than deterministic value.
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
RESULTS

Confusion Matrix
Random Forest












Probabilistic Random Forest










Accuracy
















CONCLUSION 

In Conclusion, we would like to say that Network Traffic Classification can be the perfect tool for monitoring traffic in the network as well as providing protection against DDOS and other harmful network attacks. 




































References And Code



Code
Base Paper
https://www.unb.ca/cic/datasets/nsl.html
https://robots.iopscience.iop.org

