# Introduction to Computer Science
## 360-420-DW section 02
 
 Written by: Marco Caniglia
 14 may 2019

## Distributions of Model Accuracy

## Analysis of different error types

Machine Learning Lab
Accuracy:
	When running the classification on the Breast Cancer data 1000 times, I found a mean accuracy of 96.7%. 
	Throughout the 1000 runs, the accuracy varied with S = 1.21E-4 (standard deviation). 
	The reason why the accuracy of the classification model varies between each run is because the full data set is 
	shuffled on every run with the “.shuffle” class. This means the training data, which represents 70% of the total data, 
	used to calculate the K nearest neighbors is different every time. Since 30% of the full data set is not used in the training set, 
	the classification model uses different sections of the data set and thus yield a different accuracy percentage. The accuracy of 
	this model will vary marginally with unseen data, but as seen with the very small standard deviation, the accuracy with unseen data 
	should only be different at the fourth decimal place (hence E-4).
	
	Standard Deviation:  1.2016761451516895E-4    Mean:  0.9665073170731837

Baseline:
	In order for the classification model to be perfect, all points should have the same label. Meaning the label frequency should be 
	100%. Although the model is pretty accurate (~96% accuracy), there are still some elements in the selected positive data section 
	that do not correspond to the majority of elements.

False Positive:
	A false positive element is when a data point is accepted when in reality it is not part of the positive elements. In the context 
	of medical diagnosis, a false positive is when a test result falsely indicated the condition by stating a given condition exists, 
	when it does not.

False Negative:
	On the other hand, a false negative is the lack of diagnosis. Meaning the test result indicated the given condition does not exist, 
	when in reality it does.
	
What is the difference between Recall and Precision:
	Precision can be seen as a measure of exactness or quality, whereas recall is a measure of completeness or quantity.  
	In simple terms, high precision means that an algorithm returned more relevant results than irrelevant ones, 
	and high recall means that the algorithm returned most of the relevant results.
	
	The Recall is the fraction of: (true positives)/(total positives)
	The Precision is the fraction of: (true positives)/(number of predicted positives)
	
	We can thus see that recall and precision are different measures as they calculate different proportions (although they are similar)
	
Baseline:
	A sensible baseline for both Recall and Precision would be 1 as the closer we get to 1, the more accurate our result is.
	

How do the results change with parameter k:
	After running the classification on the breast cancer data with various values of the parameter k, I observed that no matter the value 
	of k, the mean was always around 96%. Since the parameter k indicates the number of closest neighbors that are used to determine the class of an element
	area, the higher the value of k, the higher the certainty will be as the ratio of good data points to bad ones
	is much higher.