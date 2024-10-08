# Diagnosis-and-predictors-of-heart-disease

Introduction

Cardiovascular diseases remain the leading cause of death in the United States and in many developing countries. Prediction of cardiovascular disease is regarded as one of the most important subjects in the section of clinical data analysis. This makes heart disease a major concern to be dealt with. But it is difficult to identify heart disease because of several contributory risk factors such as diabetes, high blood pressure, high cholesterol, abnormal pulse rate, and many other factors. 
Prevention and early intervention are key to reducing the risk of heart disease and promoting overall heart health. Using this information as a foundation for targeted interventions can lead to better health outcomes and reduce the burden of heart disease in the population. Here we are using Heart Disease Dataset from UCI repository to do exploratory data analysis to gain insights into the relationship between different risk factors and the occurrence of heart disease.

Data Description

The dataset contains the basic patient’s information that comes from the UCI data repository. There are nearly one thousand instances in the dataset and there are 16 variables. In the first four columns, we have unique id, age, gender, location of data collection, and in the rest of the column, we have different physical conditions like chest pain type (cp), resting blood pressure (trestbps), serum cholesterol (chol), fasting blood sugar (fbs), resting electrocardiographic results (restecg), maximum heart rate achieved (thalch), exercise induced angina (exang), oldpeak — ST depression induced by exercise relative to rest, the slope of the peak exercise ST segment (slope), number of major vessels (ca) and Thalassemia (thal) and num (0 = no heart disease, 1 = heart disease).  
One of the major tasks on this dataset is to predict based on the given attributes of a patient whether that person has a heart disease or not and another is the experimental task to diagnose and find out various insights from this dataset which could help in understanding the problem more.


Hypothesis

Our aim is to determine which features have the most significant impact on predicting heart disease. This information can help prioritize interventions and preventive measures. Based on our data, we also want to find the top things to watch out for in heart patients and remind other people who do not have heart disease to avoid it. The analysis done using this dataset can aid in early diagnosis and treatment planning for individuals at risk of heart disease.

Descriptive statistics
Descriptive statistics provide a summary of the main characteristics of the dataset and understanding the distribution of each feature. Some of the common descriptive statistics include:
Number of major vessels (0-3) colored by fluoroscopy (Ca) has the most missing values however age and predicted attribute (num) did not have any missing values. The patients’ ages ranged from 28 to 77. The minimum cholesterol level in the dataset is 0. This suggests that there are some individuals with cholesterol levels of 0, which might indicate missing or invalid data. The Chol column has high variability with some individuals having very low as 0 or high as 603. The information can be used for potential identification of outliers or individuals with extreme cholesterol values. When we explore distribution of features on histogram, it reveals that Age and thalc have a normal distribution however trestbps is negatively skewed and chol and oldpeak are positively skewed.

Analysis & Results
Here we have used various visualization methods to analyze data and find out trends.

<img src="https://github.com/user-attachments/assets/9500a0f9-0369-49ef-af5b-f593e1709e0c" alt="Age_Heart disease" width="300"/>
<img src="https://github.com/user-attachments/assets/0b72d4d3-4792-45e6-8490-aadbe3142da3" alt="Gender_Heart Disease" width="300"/>

While looking at age distribution of Heart Disease, it is very common in seniors, the age group 60 and above and common among adults which belong to the age group of 41 to 60. It’s rare among the age group of 28 to 40. There was no documented records of patients syounger than 28. However, the sample size was also the largest in this age group 50-59. This information helps healthcare providers to prioritize targeted screening and prevention efforts for these age groups. While heart disease is rare in the age group of 19 to 40, it's essential to use this information to encourage young adults to develop and maintain healthy habits early on.
When we analyze gender distribution for heart disease, we can see that males are more susceptible to get heart disease than females. Males had a 2 to 3 ratio for reported heart disease, whereas women had an approximate 1 to 4 ratios. This information can help develop targeted public awareness campaigns to raise awareness about heart disease risk in men. These campaigns can highlight the specific risk factors that affect men more significantly and emphasize the importance of early detection and prevention.

<img src="https://github.com/user-attachments/assets/038e98a2-7999-412e-a31c-e468e0109aa0" alt="FastingBloodSugar_HeartDisease" width="300/">
<img src="https://github.com/user-attachments/assets/eb9ab7c3-51f1-45ae-8ce9-2e2de01fb5cf" alt="Restecg_HeartDiseae" width="300/">
 
The analysis of fasting blood sugar demonstrates that, a higher proportion of patients with heart disease have elevated fasting blood sugar levels compared to patients without heart disease. This observation may indicate a potential association between elevated fasting blood sugar and the presence of heart disease. This finding suggests that incorporating fasting blood sugar tests as part of routine health screenings, especially for individuals who may be at higher risk of heart disease will be helpful for early detection. 
ST-T abnormalities, which can indicate various cardiac and non-cardiac conditions, are more prevalent in cardiac patients compared to healthy individuals. The higher prevalence of ST-T segment changes in cardiac patients suggests that these changes are more specific to cardiac conditions, such as myocardial ischemia, myocardial infarction, or pericarditis.

<img src="https://github.com/user-attachments/assets/d9a4257c-1d34-41c6-be8d-c1af5ac7a214" alt="kde_joint_plot" width="300/">
<img src="https://github.com/user-attachments/assets/01efecb3-6729-45c7-9f69-67d173e5c519" alt="Histogram_Cholesterol_Heart disease" width="300/">

Here joint plots in seaborn helps us to understand the trend seen among two features. As observed from the above plot we can see that most of the heart disease patients in their age of upper 50s or lower 60s tend to have Cholesterol between 200mg/dl to 300mg/dl. 
The Histogram reveals that the cholesterol levels for both patients with heart disease and those without heart disease appear to be similar. However, a notable observation is that a significant number of heart disease patients have missing cholesterol values (denoted by 0). Cholesterol had some correlation to heart disease. It has a normal distribution with the mean being 199.13 and a high standard deviation of 110.78. In comparison, by omitting 0 values, the graph became positively skewed, with majority of the values being lower. The mean changed to 246.83 with a lower standard deviation of 58.53. Omitting 0 values from the data analysis represents a more accurate representation of the correlation between cholesterol and heart disease. 

<img src="https://github.com/user-attachments/assets/0bcbdee6-5615-492e-9d80-d52560684c5f" alt="ChestPainType_HeartDisease" width="300/">
<img src="https://github.com/user-attachments/assets/8a4165d1-0add-4b18-b43d-9a377e6c07ca" alt="Slope_Heart Disease" width="300/">
 
Here the analysis reveals that "asymptomatic chest pain" is the most reported chest pain among patients diagnosed with heart disease. "Asymptomatic" means "without symptoms." In the context of heart disease, it indicates that individuals who have been diagnosed with heart disease do not experience any noticeable or typical chest pain symptoms. Unlike the other types of chest pain such as "atypical angina," "non-anginal pain," and "typical angina," which are characterized by various levels of discomfort or pain in the chest. That means that a considerable number of heart disease patients may not exhibit chest pain, making it challenging to detect the presence of heart disease based solely on the presence of typical chest pain symptoms. Other diagnostic tests and risk factors may need to be considered for early detection and accurate diagnosis in individuals with asymptomatic chest pain and suspected heart disease.
In the chart, we can compare the exercise-induced ST segment changes in the electrocardiogram. The ST segment, which represents the cardiac cycle between ventricular depolarization and repolarization, provides an important aspect of interpreting exercise stress test results. The changes in ST segment behavior offer valuable insights into cardiovascular health. The chart shows that both flat and upsloping ST segment changes can be observed in both healthy individuals and cardiac patients. Higher upsloping observations in healthy individuals compared to cardiac patients reflects normal or physiological ST changes. However, the lowest observations of downsloping ST changes in healthy individuals reflects findings more specific to cardiac patients, and it could be an early sign of myocardial ischemia.

![image](https://github.com/user-attachments/assets/2bffbc1c-1a55-45b2-b7ab-3eba740a5de9)
 
The correlation heatmap used to gain insights into the dataset's structure and potential dependencies between variables. This correlation heatmap provides insight that thal (Thalassemia) is highly related to heart disease patient attribute. Exang (exercise induced angina) and ca (number of major vessels) are also correlated to heart disease patient attribute.


Conclusions

In conclusion, this data analysis study focused on exploring the relationship between different risk factors and the occurrence of heart disease using the Heart Disease Dataset from the UCI repository. This analysis revealed valuable insights on heart disease risk factors. Seniors and males are more susceptible. Elevated fasting blood sugar may be linked to heart disease. Missing cholesterol data requires caution. Asymptomatic chest pain is common among heart disease patients. Flat sloping in ST segment may indicate heart disease.  
Overall, the insights gained from this analysis can aid in prioritizing interventions, preventive measures, and healthcare strategies to reduce the burden of heart disease. The study reinforces the importance of data-driven decision-making in clinical settings and offers valuable information to healthcare providers for better patient care and heart health promotion. Prevention and early intervention remain crucial in reducing the risk of heart disease and improving overall heart health.

Limitations

Like any dataset, UCI Heart Disease dataset has certain limitations like it contains a significant number of missing values which can affect the quality of analysis if not handled appropriately, especially for machine learning. In the code we have included a way to handle missing value by replacing them with mean or mode values. Another limitation is that the dataset contains a limited number of features, which may not encompass all the relevant risk factors and variables related to heart disease. Additional relevant features could further improve the predictive performance of models. 
