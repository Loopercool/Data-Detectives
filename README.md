# Dataset 2: EV Charging Station
## Team: T09 - Data Detectives


Problems solved: Predicting charging time and energy efficiency.
As we are aware, one of the most critical aspects of machine learning is data preprocessing. In the context of regression analysis, we conducted experiments with differently preprocessed datasets across various models to compare their performance. 

Our initial data preprocessing steps included:
According to our domain knowledge we dropped some columns.
Converting START DATE and END DATE to numeric values based on their respective time zones, as indicated in the dataset (PST and PDT). We unified all PST data to PDT and transformed all date-time formats into numeric representations.
Applying label encoding to categorical columns such as Station Name, MAC Address, Address 1, and Model Number.
For addressing missing values, we tried three distinct approaches:
1. Row Deletion: We removed entire row with null values.
2. Mean/Mode Replacement: Null values were replaced with the mean (for numerical columns) or mode (for categorical columns).
3. Synthetic Data Generation using KNN: We utilized the K-nearest neighbors (KNN) algorithm to generate synthetic data points, effectively imputing missing values.
These preprocessing steps allowed us to prepare the data effectively for regression analysis, ensuring that our models were based on high-quality, processed data.

Then we used this dataset to predict: charging time and energy efficiency. 

Models we used are: 
1.	Linear Regression
2.	SGD Regression 
3.	Polynomial Regression 
4.	GradientBoosting regression
5.	RandomForest Regression

Performance Measures we used for evaluating regression models are:
1.	MSE (Mean Square Error)
2.	MAE (Mean Absolute Error)
3.	R^2

## Result for predicting charging time: 
<img width="554" alt="1" src="https://github.com/Loopercool/Data-Detectives/assets/90821913/a9d61878-ec1b-4861-b5ad-54fe9fcf917f">

<img width="555" alt="2" src="https://github.com/Loopercool/Data-Detectives/assets/90821913/003794d2-ca4c-49e5-981f-566b759ec8c3">

<img width="545" alt="3" src="https://github.com/Loopercool/Data-Detectives/assets/90821913/2eb31b32-ff26-4cc0-9be6-3170d8c6cb9f">

### Comparison using graphs:
![image](https://github.com/Loopercool/Data-Detectives/assets/90821913/8a57e9b3-f822-4347-b870-326b26b38e5b)
![image](https://github.com/Loopercool/Data-Detectives/assets/90821913/3e3fbb49-3b4d-4a12-af31-e399d6272a18)
![image](https://github.com/Loopercool/Data-Detectives/assets/90821913/7ec84922-951b-4659-86cb-6a76e435f9ec)

We got best result for deleting null rows and using random forest model for predicting.


## Result for predicting Energy Efficiency:

Energy Efficiency is defined as the ratio of energy to charging time. To calculate this, we generated a new column by combining the energy and time columns. Afterward, we removed both the original energy and time columns and proceeded to predict the energy efficiency column.

<img width="554" alt="4" src="https://github.com/Loopercool/Data-Detectives/assets/90821913/6c24eadb-d210-4250-855f-3bfec0844f30">
<img width="540" alt="5" src="https://github.com/Loopercool/Data-Detectives/assets/90821913/87f7f5df-445d-47e8-bc47-5e19a13fb86a">

### Comparison using graphs:

![image](https://github.com/Loopercool/Data-Detectives/assets/90821913/83fe462f-97ec-4ca3-bcd7-a5a1003145ef)
![image](https://github.com/Loopercool/Data-Detectives/assets/90821913/05ae81a7-d58c-4945-aff0-6254eb946105)

## Contribution:
**Preprocessing** was conducted as a **group activity** in the Mtech lab, **involving discussions** and understanding each member's perspective.   

Subsequently, **Prashuk (202101211)** utilized the dataset with deleted null values to perform Linear Regression, SGD Regression for predicting charging time and Polynomial Regression, RandomForest Regression model for predicting Energy Efficiency.

**Pratham (202101102)** employed data with null values removed for GradientBoosting Regression and  RandomForest Regression model for predicting charging time and Linear Regression, SGD Regression Energy Efficiency.

**Swara (202311005)** applied data with replacing null values using mean/mode to perform Linear Regression, SGD Regression for predicting charging time and Polynomial Regression, RandomForest Regression model for predicting Energy Efficiency.

**Diti (202311010)** utilized data replacing null values using mean/mode for GradientBoosting Regression and  RandomForest Regression model for predicting charging time and Linear Regression, SGD Regression Energy Efficiency.

Lastly, **Digant (202101403)** chose to work with data where null values were replaced using KNN for predicting charging time for Linear Regression, SGD Regression, Polynomial Regression, RandomForest Regression model.

