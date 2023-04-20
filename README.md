

# **Air Quality Prediction**

## **Backgrounds**

Air pollution is a major environmental issue that affects millions of people worldwide. Air quality is directly linked to our health and the fact that we are all at risk of air pollution. It can cause many health issues such as respiratory problems and even heart disease.

The Air Quality Index (AQI) is calculated based on the levels of several air pollutants that are known to have adverse effects on human health and the environment. These pollutants include ground-level ozone (O3), particulate matter (PM2.5 and PM10), carbon monoxide (CO), sulfur dioxide (SO2), and nitrogen dioxide (NO2). The levels of these pollutants are measured by air quality monitoring stations located in various places.

Each pollutant has its own AQI scale with breakpoints that define the different AQI levels. The AQI value for each pollutant is calculated based on its concentration and its corresponding AQI breakpoints. The overall AQI for a location is determined by the highest AQI value among all the pollutants measured.

![Hardly visible: Smog blankets Jakarta’s skyscrapers in this file photo. Air pollution in the city is among the worst in the world. (The Jakarta Post/Wendra Ajistyatama )](https://img.jakpost.net/c/2019/01/16/2019_01_16_63196_1547653415._large.jpg)


## **Objectives**
- In this project, we aim to predict air quality using machine learning algorithms. 
- By predicting air quality, we can take steps to reduce pollution levels and carry out a socially-responsive and impactful project to improve public health.
- Our goal is to develop a machine learning model that can accurately predict air quality based on historical data.


## **Methods**
- We will use The dataset from Open Data Jakarta that contains information about the Air Pollution Standard Index (ISPU) measured from 5 air quality monitoring stations (SPKU) in DKI Jakarta Province in 2021.
- We will use some algorithms such as Logistic Regression, Decision Tree, Random Forest, KNeighbors, and XGBoost Classifier to train our model

## Project Pipeline
- DATA PIPELINE
	- Required Libraries
	- Data Preparation
	- Data Gathering/ Collection
		- Import Data
		- Load Data
		- Drop Unnecessary Columns
		- Drop Duplicates
		- Summarize into function
	- Data Definition
	- Data Validation
	- Data Defense
	- Data Splitting (Train, Valid, Test)
	- EDA (on separated notebook)
		- Load Train Set
		- Check for Missing Values
		- Check for Statistical Info
		- Check for Skewness in each features
		- Check based on Classification
		- Visualize Distribution of each features
		- Visualize Pearson Correlation of the features
		- T test for each features based on Classification
		- Check Label Imbalance
		- Check for Outliers
		- Summarize for references on Data Preprocessing

- DATA PREPROCESSING
	- Required Libraries
	- Join Categories on every set (Train, Valid, Test)
	- Missing Value Handling (based on EDA Skewness) on every set
	- Feature Engineering
		- One Hot Encoding on Stasiun
		- Balancing Label
			- Undersampling
			- Oversampling
			- SMOTE
		- Label Encoding on Categori
			- Fit LE to Label Data
			- Undersampling Set
			- Oversampling Set
				- SMOTE
				- Validation Set
				- Test Set
		- Dump Dataset	

- DATA MODELING
	- Required Libraries
	- Load Configuration Files
	- Load Dataset
	- Create Training Log Template
	- Data Training
		- Create Model Object
		- Training Baseline Model
	- Data Evaluation
		- Choose The Best Baseline Model Performance using sklearn.metrics based on classification_report, roc_curve, roc_auc_score
	- Hyperparameter Tuning
	- Checking The Confusion Matrix
	
![Diagram](https://github.com/favhmu/air-quality/blob/main/assets/ml_process_system.drawio.png)	
	
- PREPARE UTIL.PY	

- PREPARE API AND STREAMLIT UI
	- Build Requirements
	- Build dockerfile
	
- CONVERTING PREPROCESSING AND MODELING INTO PYTHON SCRIPT
	- Copy-Paste every reusable functions
	- Add debug Message

- PREPARE PYTEST PYTHON SCRIPT

- BUILD REQUIREMENTS.TXT

- BUILD DOCKER-COMPOSE.YAML

- DEPLOYMENT
	- Prepare Github, DockerHub+DockerDesktop, and AWS EC2 Account
	- Setup SSH, Repository, GitHub Action and Secrets on Github
	- Setup Token and Repository on DockerHub
	- Setup Instance and Key on AWS EC2
	- CICD Design
		- Code pushed to Github	
		- Github build docker images	
		- Github push docker images to DockerHub
		- Github SSH to EC2:	
			- Cloning repository
			- Pulling large file (git Ifs pull)	
			- Pulling docker images	
			- Run docker images

## **Project Timeline**
| **Project Progress** | Week 1 | Week 2 | Week 3 | Week 4 | Week 5 | Week 6 | Week 7 | Week 8 | Week 9 | Week 10 |
|--|--|--|--|--|--|--|--|--|--|--|
| **Data collection** |**X**| | | | | | | | | |
| **Data preprocessing** |**X**|**X**| | | | | | | | |
| **Feature engineering** | | |**X**|**X**| | | | | | |
| **Model Training** | | | ||**X**|**X**|**X**|**X**| | |
| **Model Evaluation** | | | | | | | | |**X**| |
| **Model Deployment** || | | | | | | | |**X**|

## **Format Mesages Via API**
| **Success Response** | **Failed Response** |
|--|--|
|![](https://github.com/favhmu/air-quality/blob/main/assets/format-messages-via-api-and-responses_success.png)|![](https://github.com/favhmu/air-quality/blob/main/assets/format-messages-via-api-and-responses_failed.png)|
