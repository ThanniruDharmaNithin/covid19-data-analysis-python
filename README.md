# 🌍 COVID-19 Global Data Analysis using Python

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-yellow)

## 📌 Project Overview

The **COVID-19 pandemic** was one of the most significant global health crises in modern history. Governments and healthcare organizations relied heavily on **data analysis and visualization** to monitor the spread of the virus and implement effective control measures.

This project performs a **comprehensive analysis of global COVID-19 data** using Python. The study focuses on examining **confirmed cases, deaths, and recovery trends** across different countries and time periods.

Using powerful Python libraries such as **Pandas, NumPy, and Matplotlib**, this project demonstrates how real-world datasets can be cleaned, transformed, analyzed, and visualized to generate meaningful insights about the pandemic.

---

# 🎓 Course Information

**Course:** Data Analytics – Coding Ninjas
**Project Type:** Data Analytics Case Study
**Programming Language:** Python

---

# 📁 Dataset Information

Dataset used in this project:

```
covid_19_dataset.xlsx
```

The dataset contains **three primary sheets** representing different aspects of the pandemic:

| Dataset   | Description                                |
| --------- | ------------------------------------------ |
| Confirmed | Daily cumulative confirmed COVID-19 cases  |
| Deaths    | Daily cumulative deaths caused by COVID-19 |
| Recovered | Daily cumulative recovered cases           |

### Dataset Features

Each dataset includes the following columns:

* Province / State
* Country / Region
* Latitude
* Longitude
* Daily cumulative case counts from **January 22, 2020 → May 29, 2021**

The dataset includes **270+ geographic regions across the world**, enabling global comparative analysis.

---

# 🎯 Objective of the Case Study

The key objectives of this project are:

✔ Demonstrate the **practical application of Python in data analytics**
✔ Perform **data cleaning and preprocessing on real-world datasets**
✔ Identify and handle **missing values in time-series data**
✔ Analyze **confirmed cases, deaths, and recoveries**
✔ Generate **visualizations to understand pandemic trends**
✔ Perform **country-level comparative analysis**
✔ Merge multiple datasets to produce **comprehensive analytical insights**

---

# 🧰 Tools & Technologies Used

| Tool             | Purpose                           |
| ---------------- | --------------------------------- |
| Python           | Programming language for analysis |
| Pandas           | Data manipulation and cleaning    |
| NumPy            | Numerical data processing         |
| Matplotlib       | Data visualization                |
| Jupyter Notebook | Interactive analysis environment  |

---

# 🗂 Project Structure

```
covid19-global-data-analysis-python
│
├── data
│   └── covid_19_dataset.xlsx
│
├── notebooks
│   └── covid_analysis.ipynb
│
├── images
│   └── charts_and_visualizations
│
└── README.md
```

---

# 🔍 Data Analysis Workflow

The project follows a structured **data analytics pipeline** to analyze the COVID-19 dataset.

### 1️⃣ Data Loading

The datasets were imported into Python using **Pandas**, allowing the data to be stored in DataFrames for analysis and manipulation.

### 2️⃣ Data Exploration

Initial exploration was performed to understand:

* Dataset dimensions
* Column types and structures
* Presence of missing values
* Basic statistical summaries

This step helped in identifying potential data quality issues.

---

### 3️⃣ Data Cleaning

Data cleaning operations included:

* Handling missing values
* Standardizing column formats
* Replacing blank values in the **Province/State** column with **"All Provinces"**

These steps ensured that the dataset remained consistent and suitable for analysis.

---

### 4️⃣ Data Transformation

Data transformations included:

* Aggregating statistics at the **country level**
* Calculating **recovery rates and death rates**
* Restructuring datasets for easier analysis

This step made it easier to perform comparative country analysis.

---

### 5️⃣ Dataset Merging

The confirmed, deaths, and recovered datasets were merged to create a **comprehensive dataset representing the pandemic’s impact across countries and time**.

This combined dataset allowed deeper analytical insights into the relationship between cases, deaths, and recoveries.

---

### 6️⃣ Data Visualization

Various visualizations were created to better understand global pandemic trends.

Examples include:

📈 Confirmed cases growth over time
📉 Death rate comparisons between countries
📊 Recovery statistics by region

Visualizations helped highlight patterns and trends in the pandemic progression.

---

# 📊 Key Insights

Some important insights obtained from the analysis include:

* COVID-19 cases increased rapidly during the early stages of the pandemic.
* Several countries experienced significantly higher case surges compared to others.
* Recovery rates improved over time due to improved healthcare responses and treatment strategies.
* Visualizations clearly showed **multiple pandemic waves across different regions**.

---

# 📈 Results

The analysis demonstrates how **data analytics techniques can be applied to real-world global health datasets**.

Using Python and analytical libraries, the project successfully:

* Processed large real-world datasets
* Generated meaningful analytical insights
* Visualized global pandemic trends effectively

This highlights the importance of **data-driven decision making during global crises**.

---

# ▶️ How to Run the Project

Follow the steps below to run the analysis locally.

### 1️⃣ Clone the repository

```
git clone https://github.com/ThanniruDharmaNithin/covid19-global-data-analysis-python.git
```

### 2️⃣ Navigate to the project folder

```
cd covid19-global-data-analysis-python
```

### 3️⃣ Install required libraries

```
pip install pandas numpy matplotlib
```

### 4️⃣ Launch Jupyter Notebook

```
jupyter notebook
```

Open the analysis notebook and run the cells to reproduce the results.

---

# 📚 Skills Demonstrated

This project demonstrates important **Data Analytics skills**, including:

* Data Cleaning
* Data Transformation
* Exploratory Data Analysis (EDA)
* Data Visualization
* Time Series Analysis
* Real-world Dataset Handling
* Python-based Analytical Workflow

---

# 📌 Learning Outcomes

Through this case study, the following competencies were developed:

* Practical data analysis using Python
* Handling real-world time-series datasets
* Extracting insights from global datasets
* Building analytical workflows for decision making

---

# 👨‍💻 Author

**Thanniru Dharma Nithin**

Aspiring Data Analyst passionate about transforming raw data into meaningful insights.

GitHub Profile:
https://github.com/ThanniruDharmaNithin

---

⭐ If you found this project useful, consider giving the repository a star!
