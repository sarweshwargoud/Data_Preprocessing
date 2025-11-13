📌 Data Cleaning & Preprocessing – Titanic Dataset
📖 Overview

This project focuses on data cleaning, preprocessing, and preparation using the popular Titanic Dataset.
The goal is to transform raw data into a clean, structured format suitable for machine learning models.

This task is part of the AI/ML Internship – Task 1: Data Preprocessing.

🗂️ Project Structure
Data_Preprocessing_Task/
│
├── notebook.ipynb          # Complete preprocessing code
├── cleaned_titanic.csv     # Final cleaned dataset
├── data/
│     └── titanic.csv       # Original dataset
└── README.md               # Project documentation

🧹 Steps Performed (Data Cleaning + Preprocessing)
1. Data Loading & Exploration

Loaded dataset using Pandas

Displayed:

head()

info()

describe()

Missing values summary

Checked data types and distributions

2. Handling Missing Values

Age → Filled using median

Embarked → Filled using mode

Cabin → Dropped due to many missing values

Fare → Filled with median (if missing)

3. Encoding Categorical Variables

Sex → Label Encoding (male=1, female=0)

Embarked → One-Hot Encoding (Embarked_Q, Embarked_S)

4. Feature Scaling

Used StandardScaler to scale continuous variables:

Age

Fare

Scaling helps machine learning models converge faster and perform better.

5. Outlier Detection & Removal

Used IQR (Interquartile Range) method on Fare:

IQR = Q3 - Q1
Lower bound = Q1 - 1.5 * IQR
Upper bound = Q3 + 1.5 * IQR


Removed rows with fare values outside this range.

6. Data Visualization

Used boxplots to visualize outliers for numerical features

Checked distribution before & after preprocessing

7. Saving Cleaned Data

Exported the final processed dataset as:

cleaned_titanic.csv

🛠️ Tools & Libraries Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-Learn

📝 How to Run This Project

Open notebook.ipynb

Ensure the dataset is available in data/titanic.csv

Run all cells sequentially

Cleaned dataset will be generated as cleaned_titanic.csv

📎 Dataset Source

Kaggle Titanic Dataset:
https://www.kaggle.com/datasets/yasserh/titanic-dataset

🎯 Outcome

You will learn:

Handling missing data

Encoding categorical variables

Standardizing numerical columns

Detecting and removing outliers

Preparing data for building machine learning models