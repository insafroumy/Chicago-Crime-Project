# 🔍 Chicago Crime Analysis (2001–2022)
 
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas) ![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c) ![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-4c8cbf) ![Statsmodels](https://img.shields.io/badge/Statsmodels-Time%20Series-orange)
 
---
 
## 📌 Project Overview
 
This project performs an in-depth exploratory data analysis (EDA) on over **3 million crime records** from the City of Chicago spanning **2001 to 2022**. The dataset is sourced from multiple CSV files packed within a ZIP archive and merged into a unified DataFrame for analysis.
 
The analysis covers six core topics: district-level comparisons, yearly crime trends, rush-hour patterns, monthly seasonality, holiday crime spikes, and time series decomposition.
 
---
 
## 📂 Dataset
 
- **Source:** Chicago Crime Dataset (2001–2022), provided as a ZIP archive containing yearly CSV files
- **Size:** ~3,017,826 records across 9 columns
- **Key Columns:** `Date`, `Primary Type`, `District`, `Location Description`, `Arrest`, `Domestic`, `Latitude`, `Longitude`
---
 
## 🛠️ Technologies Used
 
| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, grouping, resampling |
| `numpy` | Numerical operations & missing value handling |
| `matplotlib` | Custom visualizations |
| `seaborn` | Statistical plot styling |
| `statsmodels` | Time series decomposition (seasonal_decompose) |
| `scipy` | Peak detection in seasonal signals |
| `holidays` | U.S. holiday calendar mapping |
| `zipfile` | Reading CSV files directly from ZIP archive |
 
---
 
## 📊 Analysis Topics
 
### 1️⃣ Comparing Police Districts (2022)
- Filtered crimes to the year 2022 and grouped by police district
- **District 8** had the **highest** number of crimes
- **District 31** had the **lowest** number of crimes
- Visualized as a bar chart sorted by crime count
### 2️⃣ Crime Trends Across the Years
- Resampled crime data yearly to identify the overall trend
- **Overall crime is decreasing** over the 2001–2022 period
- However, several crime types **bucked the trend** and increased:
  - 📈 Weapons Violation
  - 📈 Criminal Sexual Assault
  - 📈 Motor Vehicle Theft (spike post-2020)
  - 📈 Stalking
  - 📈 Concealed Carry License Violation
  - 📈 Human Trafficking
### 3️⃣ AM vs. PM Rush Hour Crimes
- **AM Rush Hour:** 7:00 AM – 10:00 AM
- **PM Rush Hour:** 4:00 PM – 7:00 PM
- **PM rush hour has more crimes** than AM rush hour
- **Top 5 crimes during AM Rush Hour:** Theft, Battery, Criminal Damage, Narcotics, Assault
- **Top 5 crimes during PM Rush Hour:** Theft, Battery, Criminal Damage, Narcotics, Assault
### 4️⃣ Monthly Crime Patterns
- Resampled data monthly and broke down by crime type
- Crimes that **increased post-2020** against the overall decreasing trend:
  - Weapons Violation, Human Trafficking, Deceptive Practice, Homicide, Motor Vehicle Theft, Stalking
### 5️⃣ Holiday Crime Analysis
- Mapped each crime record to U.S. federal holidays using the `holidays` library
- **Top 3 holidays with the most crimes:**
| Rank | Holiday | Top Crime |
|---|---|---|
| 🥇 1st | New Year's Day | Theft (6,845 incidents) |
| 🥈 2nd | Independence Day | Battery (5,805 incidents) |
| 🥉 3rd | Labor Day | Battery (4,607 incidents) |
 
- Top 5 crimes per holiday were visualized as bar charts
### 6️⃣ Seasonality Analysis (Time Series Decomposition)
- Focused on **Theft** as a representative crime type
- Applied **3-month rolling average** for smoothing
- Used `statsmodels.tsa.seasonal_decompose` to extract trend, seasonal, and residual components
- Used `scipy.signal.find_peaks` to detect seasonal peaks
- **Key finding:** Theft exhibits a clear **annual seasonal cycle**, with a peak-to-trough amplitude of approximately **6,236 crimes/month**
---
 
## 🚀 How to Run
 
1. Clone the repository:
```bash
git clone https://github.com/insafroumy/Chicago-Crime-Project.git
```
 
2. Open `Chicago_Crime.ipynb` in **Google Colab** or **Jupyter Notebook**
3. Mount your Google Drive and ensure the dataset ZIP file is placed at:
```
MyDrive/AXSOSACADEMY/AXSOSACADEMY/AdvancedML-06/Week22/Data/Chicago_Crime_2001-2022.zip
```
 
4. Run all cells in order
---
 
## 📁 Repository Structure
 
```
Chicago-Crime-Project/
│
├── Chicago_Crime.ipynb      # Main analysis notebook
└── README.md                # Project documentation
```
 
---
 
## 🔑 Key Insights
 
- 📉 Chicago's overall crime rate has been **declining since 2001**
- 🔫 **Weapons violations and sexual assault** are among the few crimes **increasing** in recent years
- 🌙 **PM rush hour** is significantly more dangerous than AM rush hour
- 🎆 **New Year's Day** is the most crime-heavy U.S. holiday in Chicago
- 📅 Theft follows a **strong annual seasonal cycle**, peaking in summer months
---
 
## 👩‍💻 Author
 
**Insaf AlRumi**  
Computer Systems Engineering Graduate | Data Science & ML Bootcamp — AXSOS Academy  
[GitHub](https://github.com/insafroumy) | [LinkedIn](https://www.linkedin.com/in/insaf-alrumi)
 

