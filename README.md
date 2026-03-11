# \# 🌍 COVID-19 Global Data Analysis – Case Study

# 

# \## 📊 Overview

# The COVID-19 pandemic, caused by the SARS-CoV-2 virus, emerged in late 2019 and rapidly spread across the globe. Governments and healthcare organizations relied heavily on \*\*data-driven insights\*\* to track the spread of the virus, allocate healthcare resources, and implement control measures.

# 

# This project performs a \*\*comprehensive analysis of global COVID-19 data\*\* using Python. The analysis focuses on confirmed cases, deaths, and recoveries across countries and regions over time.

# 

# Using Python libraries such as \*\*Pandas, NumPy, and Matplotlib\*\*, the project demonstrates how real-world datasets can be cleaned, transformed, visualized, and analyzed to uncover meaningful insights about the pandemic.

# 

# ---

# 

# \# 📁 Dataset Information

# 

# Dataset used:

# 

# covid\_19\_dataset-1718175635.xlsx

# 

# The dataset consists of three sheets:

# 

# | Dataset | Description |

# |--------|-------------|

# | Confirmed | Daily cumulative confirmed COVID-19 cases |

# | Deaths | Daily cumulative deaths caused by COVID-19 |

# | Recovered | Daily cumulative recovered patients |

# 

# \### Dataset Features

# 

# Each dataset includes the following columns:

# 

# \- Province/State  

# \- Country/Region  

# \- Latitude  

# \- Longitude  

# \- Daily case counts (Jan 22, 2020 → May 29, 2021)

# 

# The data contains \*\*276+ geographic regions worldwide\*\*.

# 

# ---

# 

# \# 🎯 Objectives of the Case Study

# 

# The key objectives of this project include:

# 

# ✔ Demonstrate practical use of \*\*Python for data analysis\*\*  

# ✔ Perform \*\*data cleaning and preprocessing\*\*  

# ✔ Handle \*\*missing values in time-series datasets\*\*  

# ✔ Analyze confirmed cases, deaths, and recoveries  

# ✔ Generate visualizations to understand trends  

# ✔ Perform comparative country analysis  

# ✔ Merge datasets for deeper insights

# 

# ---

# 

# \# ⚙️ Tools and Technologies

# 

# | Tool | Purpose |

# |-----|--------|

# | Python | Data analysis programming |

# | Pandas | Data manipulation |

# | NumPy | Numerical computation |

# | Matplotlib | Data visualization |

# | Jupyter Notebook | Analysis environment |

# 

# ---

# 

# \# 🧹 Data Processing Workflow

# 

# The project followed a structured data analysis workflow.

# 

# \## 1️⃣ Data Loading

# 

# The datasets were loaded using Pandas.

# 

# ```python

# import pandas as pd

# 

# confirmed = pd.read\_excel("covid\_19\_dataset.xlsx", sheet\_name="Confirmed")

# deaths = pd.read\_excel("covid\_19\_dataset.xlsx", sheet\_name="Deaths")

# recovered = pd.read\_excel("covid\_19\_dataset.xlsx", sheet\_name="Recovered")

# ```

# 

# ---

# 

# \# 🔍 Data Exploration

# 

# Initial exploration was performed to understand the dataset structure.

# 

# Key checks performed:

# 

# \- Number of rows and columns  

# \- Data types  

# \- Missing values  

# \- Summary statistics  

# 

# Example:

# 

# ```python

# confirmed.info()

# confirmed.describe()

# ```

# 

# ---

# 

# \# 🧽 Handling Missing Data

# 

# Missing values were identified and handled using forward fill.

# 

# ```python

# confirmed.fillna(method="ffill", inplace=True)

# deaths.fillna(method="ffill", inplace=True)

# recovered.fillna(method="ffill", inplace=True)

# ```

# 

# ---

# 

# \# 🧼 Data Cleaning and Preparation

# 

# Blank values in the Province/State column were replaced.

# 

# ```python

# df\["Province/State"].fillna("All Provinces", inplace=True)

# ```

# 

# This ensures consistent geographic information.

# 

# ---

# 

# \# 📈 Exploratory Data Analysis

# 

# \## Global Confirmed Cases Trend

# 

# Country-level trends were analyzed by grouping the dataset.

# 

# ```python

# country\_data = confirmed.groupby("Country/Region").sum()

# ```

# 

# Line plots were generated to visualize the spread of COVID-19 over time.

# 

# ---

# 

# \## China Case Trend

# 

# China's confirmed cases were analyzed separately to study the initial outbreak and the effect of containment measures.

# 

# ---

# 

# \# 📊 Country-Level Analysis

# 

# \## Peak Daily New Cases

# 

# Daily new cases were calculated using the difference between consecutive days.

# 

# Daily New Cases = Current Day Total − Previous Day Total

# 

# Countries analyzed:

# 

# \- Germany

# \- France

# \- Italy

# 

# The analysis identified which country experienced the highest single-day surge and the corresponding date.

# 

# ---

# 

# \## Recovery Rate Comparison

# 

# Recovery Rate = Recoveries / Confirmed Cases

# 

# The recovery rates of \*\*Canada and Australia\*\* were compared to evaluate pandemic management effectiveness.

# 

# ---

# 

# \## Death Rate Distribution in Canada

# 

# Death Rate = Deaths / Confirmed Cases

# 

# Province-level analysis helped identify:

# 

# \- Province with the highest death rate

# \- Province with the lowest death rate

# 

# ---

# 

# \# 🔄 Data Transformation

# 

# The deaths dataset was transformed from \*\*wide format to long format\*\*.

# 

# ```python

# deaths\_long = deaths.melt(

# &nbsp;   id\_vars=\["Province/State","Country/Region","Lat","Long"],

# &nbsp;   var\_name="Date",

# &nbsp;   value\_name="Deaths"

# )

# ```

# 

# Benefits:

# 

# \- Easier time-series analysis

# \- Simplified merging of datasets

# 

# ---

# 

# \# 🌎 Global Death Analysis

# 

# Key analyses performed:

# 

# \- Total number of deaths per country

# \- Top 5 countries with highest average daily deaths

# \- Death trend evolution in the United States

# 

# ---

# 

# \# 🔗 Data Merging

# 

# The confirmed, deaths, and recovered datasets were merged.

# 

# ```python

# merged\_data = confirmed\_long.merge(deaths\_long, on=\["Country/Region","Date"])

# merged\_data = merged\_data.merge(recovered\_long, on=\["Country/Region","Date"])

# ```

# 

# This created a comprehensive dataset for pandemic analysis.

# 

# ---

# 

# \# 📅 Monthly Pandemic Progression

# 

# Monthly aggregates were calculated to understand pandemic waves.

# 

# Metrics analyzed:

# 

# \- Monthly confirmed cases

# \- Monthly deaths

# \- Monthly recoveries

# 

# Country comparisons included:

# 

# \- United States

# \- Italy

# \- Brazil

# 

# ---

# 

# \# 📊 Combined Dataset Insights

# 

# \## Countries with Highest Average Death Rates

# 

# Using the merged dataset, the countries with the highest death rates were identified.

# 

# Possible reasons include:

# 

# \- Healthcare system capacity

# \- Population demographics

# \- Testing and reporting differences

# 

# ---

# 

# \## South Africa Case Outcomes

# 

# Recovery vs death comparisons showed that recoveries significantly outnumbered deaths.

# 

# ---

# 

# \## U.S. Monthly Recovery Ratio

# 

# Recovery Ratio = Recoveries / Confirmed Cases

# 

# Monthly analysis from \*\*March 2020 to May 2021\*\* showed improvements in recovery ratios over time.

# 

# ---

# 

# \# 📊 Key Insights

# 

# Important insights from the analysis:

# 

# \- COVID-19 cases increased rapidly during the early stages of the pandemic.

# \- Recovery rates improved over time due to better treatment and healthcare strategies.

# \- Death rates varied significantly between countries.

# \- Multiple pandemic waves were visible in the time-series data.

# 

# ---

# 

# \# 🧠 Learning Outcomes

# 

# Through this project, the following skills were developed:

# 

# \- Data cleaning and preprocessing

# \- Handling missing data

# \- Time-series data analysis

# \- Data transformation

# \- Dataset merging

# \- Data visualization

# 

# ---

# 

# \# ✅ Conclusion

# 

# This case study demonstrated how Python can be used to analyze large-scale real-world datasets.

# 

# Through data cleaning, transformation, and visualization, the project explored the global progression of COVID-19 and generated meaningful insights about pandemic trends.

# 

# The study highlights the importance of \*\*data analytics in understanding global health crises and supporting informed decision-making\*\*.

# 

# ---

# 

# \# 👨‍💻 Author

# 

# \*\*Thanniru Dharma Nithin\*\*

# 

# Aspiring Data Analyst passionate about transforming raw data into actionable insights.

# 

# GitHub Profile:  

# https://github.com/ThanniruDharmaNithin

# 

# ⭐ If you found this project helpful, consider giving the repository a star!

