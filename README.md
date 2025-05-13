# 📲 Push Notification A/B Test

This project demonstrates how to simulate and analyze an A/B experiment aimed at improving app engagement through a new push notification mechanic. The analysis includes data validation, conversion analysis, behavioral segmentation, and statistical testing using Python.

📘 **Full project description is available [here](https://iridescent-talon-964.notion.site/Push-Notification-A-B-Test-Analysis-1f2ed80500f880159c1bd4a3723dfcc6)**

---

## 📊 Workflow Overview

### 1. 📦 Data Simulation (Python)  
- A synthetic dataset was generated to simulate user behavior over 7 days.  
- Each user received a push notification either in Group A (control) or Group B (test).  
- Time of notification was randomized to imitate real conditions.  
- Data fields included: user ID, group, notification time, open time, and derived features.

### 2. 📐 Feature Engineering & Validation  
- Created a binary `opened_app` feature.  
- Calculated `time_to_open` in minutes.  
- Checked:
  - Group sizes  
  - Randomness of assignment (Chi-square test)  
  - Distribution of events by day  

### 3. 🧪 Statistical Analysis  
- Compared **conversion rates** between groups (Chi-square and Z-test):  
  - 📉 Group A CR ≈ 24.7%  
  - 📈 Group B CR ≈ 31.5%  
  - ✅ Statistically significant (p = 0.0002)  
- Compared **time to open app** (Mann–Whitney U test):  
  - Slightly higher in Group B  
  - ❌ Not statistically significant (p = 0.0569)

### 4. 📅 Daily Dynamics Visualization  
- Tracked:
  - Number of notifications sent per group per day  
  - Number of app opens per day  
  - Conversion spikes (e.g., May 4 in Group A)  
- Found slight anomalies (fewer notifications yet higher open rate on May 4)

---

## 📁 Files in this Repository  
- `Ab test meditation push - data generation.ipynb`: script to create the synthetic dataset  
- `ab_test_meditation_push.ipynb`: full A/B test analysis and visualizations  
- `requirements.txt`: list of required Python libraries  
- `README.md`: project documentation  
