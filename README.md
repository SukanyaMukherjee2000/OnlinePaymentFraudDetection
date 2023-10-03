# OnlinePaymentFraudDetection
Report : online payment fraud detection
Our data in hand has 11 variables and 6362619 observations on payer’s information. 
I have conducted an in-depth analysis and prediction using different classification models and compared their accuracy score to determine the best model suited for our data. 


-> Upon exploring the data we observe the following: 
•	The dataset contains no null values
•	Among the 5types of online transaction cash out has the maximum frequency followed by payment method
•	Fraud payment has significantly lower value than non fraud payments in the dataset. 
•	We observe that maximum fraud payments have taken place in transfer and cash out payment methods. 



This is an unbalanced data so removing the outliers will remove the required data. From boxplots of different variables we can find that there are lots of outliers present in each features. So after dropping the outliers using IQR method, we deleted almost all fraud transactions from the data frame. Only 26 fraud transactions remain in the entire data frame. So removing outliers in this case is not a good option. Upon performing EDA it is observed that maximum transactions have taken place in cash out and payment method. 



Now looking at the correlation plot we can find that there is a high correlation between the initial amount of the recipient before and after the transaction. Also, there is a correlation of the balance before and after the transaction. We can find positive correlation of amount with both initial balance of the recipient before and after the transaction.



Now to deal with imbalanced dataset we perform resampling and now the number of observation for fraud transactions and not fraud transactions are equal. 



Now that our dataset is clean it is ready for predictive modelling. We divide our dataset into train and test data in 80:20 ratio and fit Decision Tree , logistics regression,linear discriminant analysis, k nearest neighbour classifier and GaussianNB.  
Here our decision tree and KNN gives an accuracy of 99% so it shows over fitting of the model. Whereas our logistic regression gives 90% accuracy and LDA gives 79% accuracy. GaussianNB has the lower accuracy 64%. So we can say our logistic regression is the best model among all.  
	
