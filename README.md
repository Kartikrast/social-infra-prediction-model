# 🏛️ Social Infrastructure Prediction Model

[![Project Status](https://img.shields.io/badge/status-active-brightgreen)](https://github.com/Kartikrast/social-infra-prediction-model)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://python.org)
[![License](https://img.shields.io/github/license/Kartikrast/social-infra-prediction-model)](LICENSE)

---

## 📝 Project Overview

**Type:** Exploratory Data Analysis (EDA)  
**Contribution:** Individual  
**Repository:** [GitHub Link](https://github.com/Kartikrast/social-infra-prediction-model)

This project analyzes real-world data on hospitals, preschools, and secondary schools across the Samarkand region to assess and predict infrastructure needs. It aims to support evidence-based planning and resource allocation in health and education, empowering policymakers and development agencies to drive sustainable, people-centric improvements.

---

## 📊 Data Insights

This project brings together multiple real-world datasets to assess and predict infrastructure needs across   **secondary schools**, **preschools**, and **hospitals** in the Samarkand region.

---

### 🎓 Secondary Schools

- **Data Source:** Secondary school infrastructure dataset (Samarkand region).  
- **Key Features:** School name, location, infrastructure conditions, resources, accessibility, satisfaction, and population indicators.  
- **Dataset Information:**
  - **Rows:** 1261  
  - **Columns:** 109  
  - **Duplicate Rows:** 0 (✅ No duplicates found)
- **Data Cleaning Summary:**
  - *Columns dropped where all rows were `0`*  
  - *Columns with more than `1000` null values*  
  ➤  
    - `Russian` (1164 missing)
    - `Tajik` (1235 missing)
    - `Enter the type of wall material of the building:.1 ` (1137 missing)
    - `Condition of the building walls.2 ` (1137 missing)
    - `Do you consider the building safe during an earthquake?.2 ` (1137 missing)
    - `Enter the type of roofing material of the building.1 ` (1137 missing)
    - `Condition of the building roof.2 ` (1137 missing)
    - `Condition of windows and frames in classrooms.2 ` (1137 missing)
    - `Condition of the floors in classrooms.2 ` (1137 missing)
    - `Condition of the doors in classrooms.2 ` (1137 missing)
    - `What is the condition of the adapted (community-built, sponsored, stone, wood, or adobe) restroom? ` (1147 missing)

  ⮕ These were dropped due to excessive missing data.

  - *Columns with more than `100` null values* 

     ➤   

    - `If completed, enter the year` (406 missing)
    - `Enter the type of wall material of the building:` (688 missing)
    - `Condition of the building walls.1` (688 missing)
    - `Do you consider the building safe during an earthquake?.1` (689 missing)
    - `Enter the type of roofing material of the building:` (690 missing)
    - `Condition of the building roof.1` (691 missing)
    - `Condition of windows and frames in classrooms.1` (691 missing)
    - `Condition of the floors in classrooms.1` (691 missing)
    - `Condition of the doors in classrooms.1` (691 missing)
    - `What is the condition of the standard (project-based) restroom?` (179 missing)

  ⮕ Dropped or imputed depending on importance and relevance.

  - *Redundant/Repetitive Columns*  
    ➤ 
     - `Condition of the building walls.1`  
     - `Do you consider the building safe during an earthquake?.1`  
     - `Condition of the building roof.1`  
     - `Condition of windows and frames in classrooms.1`  
     - `Condition of the floors in classrooms.1`  
     - `Condition of the doors in classrooms.1` 
  ⮕ Many of these appeared multiple times; only unique, relevant fields were retained.



✅ *All the above columns were removed to ensure cleaner and more accurate analysis.*

  - **Total Rows (after data cleaning):** 1,261  
  - **Total Columns (after data cleaning):** 79 

- **Dataset Bifurcation:**

    - Population 
    - Infrastructure
    - Resources
- **Variables Description:**

    We have bifurcated the dataset into 3 different dataframes: population_df, infrastructure_df, and resources_df.
    Each of these dfs have their own related columns, on which we will be performing analysis. The idea to bifurcate the dataset is to make the analysis more focused and easier to understand. 

    Using this bifurcation we will simplfy the current position of each school in terms of capacity, infrastructure and resources. Once these positions are framed we can then use them as scores for each school in order to identify the level of development needed for each school.

 

### 🧒 Preschool Facilities Dataset
- **Data Source:** Preschool infrastructure dataset (Samarkand region)
- **Key Features:** Design capacity, total students, staff count, year built, wall/roof condition, water availability, electricity condition, heating source, presence of fence.
- **Dataset Information:**
  - **Rows:** 491  
  - **Columns:** 75  
  - **Duplicate Rows:** 0 (✅ No duplicates found)
- **Data Cleaning Summary:**
  - *Columns dropped where all rows were `0`*    
  ➤  
    - `Building foundations`  
    - `Condition of the concrete slabs (ceilings) between floors`  
    - `Are there concrete/asphalt pathways between the buildings and outdoor restrooms?`  
    - `Do you think the restroom is safe for children?`  
    - `Do you think there is a connection between the condition of restrooms and children's willingness to attend school?`  
    - `Is the pathway to the restroom illuminated with lights and safe for children?`  
    - `Conditions for dining`


  - *we have to drop the comments column as well* 

✅ *All the above columns were removed to ensure cleaner and more accurate analysis.*

  - **Total Rows (after data cleaning):** 491  
  - **Total Columns (after data cleaning):** 67 

- **Dataset Bifurcation:**

    - Population 
    - Infrastructure
    - Resources
- **Variables Description:**

    We have bifurcated the dataset into 3 different dataframes: population_df, infrastructure_df, and resources_df.
    Each of these dfs have their own related columns, on which we will be performing analysis. The idea to bifurcate the dataset is to make the analysis more focused and easier to understand. 

    Using this bifurcation we will simplfy the current position of each school in terms of capacity, infrastructure and resources. Once these positions are framed we can then use them as scores for each school in order to identify the level of development needed for each school.

- **Scoring:**    
  - Scoring categorical columns
  - Scoring numerical columns

    - Static numerical columns
    - Range numerical columns 
 

### 🏥 Hospital Infrastructure Dataset

- **Data Source:** Hospital infrastructure dataset (Samarkand region)  
- **Key Features:** Electricity supply, heating source, water availability, restroom condition, sewage system, generator availability, fire safety, earthquake resistance, CCTV presence, nearby transport access  
- **Dataset Information:**
  - **Rows:** 280  
  - **Columns:** 55  
  - **Duplicate Rows:** 0 (✅ No duplicates found)
- **Data Cleaning Summary:**
  - *Columns dropped where all rows were `0`*  
  ➤  
    - `Building foundations`  
    - `Condition of the concrete slabs (ceilings) between floors`  
    - `Are there concrete/asphalt pathways between the buildings and outdoor restrooms?`  
    - `Do you think the restroom is safe for patient?`  
    - `Is the pathway to the restroom illuminated with lights and safe for patient?`



✅ *All the above columns were removed to ensure cleaner and more accurate analysis.*

  - **Total Rows (after data cleaning):** 280  
  - **Total Columns (after data cleaning):** 50 

- **Dataset Bifurcation:**

    - Population 
    - Infrastructure
    - Resources
- **Variables Description:**

    We have bifurcated the dataset into 3 different dataframes: population_df, infrastructure_df, and resources_df.
    Each of these dfs have their own related columns, on which we will be performing analysis. The idea to bifurcate the dataset is to make the analysis more focused and easier to understand. 

    Using this bifurcation we will simplfy the current position of each school in terms of capacity, infrastructure and resources. Once these positions are framed we can then use them as scores for each school in order to identify the level of development needed for each school.


- **Scoring:**    
  - Scoring categorical columns
  - Scoring numerical columns

    - Static numerical columns
    - Range numerical columns 

---



## 🎓 Secondary Schools

### 🔍 Exploratory Data Analysis Highlights

- **Univariate Analysis:**

  - Analyzed infrastructure indicators like wall, roof, and heating conditions across schools.
  - Evaluated availability of core resources: electricity, clean water, heating systems, and student restrooms.
  - Population metrics like usage % and z-scores revealed high variation in school accessibility and demand.

- **Bivariate & Multivariate Analysis:**

  - Compared infrastructure scores with satisfaction and distance-to-school to uncover inequality clusters.
  - Explored relationships between population scores, usage %, and resource availability to assess pressure on infrastructure.
  - Visual tools like heatmaps and barplots helped spot regional disparities in facility quality.

- **Visualizations:**

  - We can see that the usage % is normally distributed but there are values where the usage is more than 100% making the school overcrowded 
  - On the other hand there are values where the usage is less than 50% making the school underutilized

---

### 🧮 Predictive Modeling

- **Techniques:** Classification and regression were used to model school satisfaction and infrastructure adequacy.
- **Scoring System:** Developed composite scores (infra/resource/population) for multi-dimensional comparison.
- **Evaluation:** Applied grid search and validation to fine-tune school-level prediction performance.

---

### 💡 Key Insights & Impact

- **Infrastructure Disparity:** Some schools meet modern standards while others lack basics like heating or lighting.
- **Resource Imbalance:** Many schools with poor infrastructure still serve large student populations.
- **Accessibility Gaps:** Schools farthest from residential areas tend to have lower satisfaction, especially where public transport is limited.

---

### 🚀 Future Opportunities: LLMs & GPT for Human Interaction

- **Natural Language Search:** Query data using prompts like “List schools with no gym and heating below average.”
- **Automated Briefs:** Generate planning reports per district showing satisfaction gaps and renovation needs.
- **AI Chat Support:** Help education planners explore school stats by typing questions instead of filtering Excel files.

---

### ⏭️ Next Steps

- Finalize per-school renovation index using combined infrastructure/resource/population scores.
- Create dashboards for district-level education authorities to plan funding.
- Extend approach to analyze private or vocational secondary institutions.

---

### 📌 Conclusion

This secondary school analysis offers a data-driven lens on educational infrastructure. By combining detailed EDA, scoring systems, and AI-readiness, it supports smarter investments and sustainable learning environments. The project bridges raw infrastructure data with actionable insights that can guide real-world education planning.


---

## 🧒 Preschools
### 🔍 Exploratory Data Analysis Highlights

* **Univariate Analysis:**

  * Investigated design capacity, student/staff count, and restroom conditions.
  * Examined prevalence of safety features, internet access, and structural conditions.

* **Bivariate & Multivariate Analysis:**

  * Analyzed how infrastructure (electricity, heating, water) relates to population usage and satisfaction.
  * Compared utilization scores across districts to flag under- or over-utilized kindergartens.

* **Visualizations:**

  * Over 15 plots: utilization histograms, infrastructure bar charts, heatmaps, satisfaction trends.
  * Visuals emphasized planning needs and condition gaps.

---

### 🧑‍🤝‍🧑 Population Utilization Scoring

A Gaussian-based scoring system was developed to evaluate population efficiency.

* **Total Population** = total\_students + staff\_total
* **Utilization Ratio** = total\_population / design\_capacity
* **Ideal Utilization** = 85%
* **Scoring:** Gaussian function centered at 0.85, scoring from 0 (inefficient) to 1 (optimal)
* **Labels Assigned:**

  * ✅ Ideal
  * ⚠️ Acceptable
  * ❌ Needs Review

This logic ensures:

* Balanced infrastructure usage
* Identification of over/under-crowded facilities
* Informed planning for expansions

---

### 🧮 Predictive Modeling

* **Techniques:** Applied classification and scoring models to predict utilization performance and satisfaction.
* **Evaluation:** Validated scoring against infrastructure quality and population load.
* **Impact:** Highlights where upgrades or redistribution of population are most needed.

---

### 💡 Key Insights & Impact

* **Over- & Under-Capacity:** Some preschools operate well beyond or below optimal design thresholds.
* **Infrastructure-Satisfaction Link:** Facilities with better utilities and restrooms correlate with higher satisfaction.
* **Accessibility Gap:** Rural kindergartens with long commute distances show lower utilization.

---

### 🚀 Future Opportunities

* Add real-time monitoring of preschool population changes.
* Integrate LLMs for querying capacity planning needs.
* Recommend construction or consolidation of facilities based on demand clusters.

---

### ⏭️ Next Steps

* Finalize integration of utilization scores into broader planning dashboards.
* Share recommendations with early childhood education planners.
* Expand scoring model to incorporate seasonal/temporal enrollment variation.

---

### 📌 Conclusion

This preschool infrastructure analysis introduces a data-driven approach to monitor and optimize population capacity and facility readiness. The Gaussian utilization logic offers a smart, interpretable method to support policy and funding decisions for sustainable preschool infrastructure planning.

---

## 🏥 Hospitals

### 🔍 Exploratory Data Analysis Highlights

- **Data Separation:**  
  The dataset was divided into three parts based on feature types:  
  - **Infrastructure features** (e.g., building condition, electricity, heating)  
  - **Resource availability** (e.g., staff count, amenities, utilities)  
  - **Population and usage** (e.g., student count, patient load, capacity)

- **Preprocessing Steps:**  
  - We handle Missing values appropriately based on context, and columns that were completely null were identified and removed.
  - Columns were renamed for clarity and a unique ID was added to each row to facilitate merging and tracking.
  - Categorical information like heating type, wall material, and internet availability was extracted to better understand facility conditions.  
  - Numerical columns were identified based on data types for further analysis.

- **Univariate Analysis:**  
    - Examined the distribution of year built, patient counts, and infrastructure conditions.  
    - Identified clusters of older buildings and facilities in poor condition, highlighting areas most in need of renovation.

- **Bivariate/Multivariate Analysis:**  
    - Used pairplots and heatmaps to uncover patterns, such as facilities with poor heating often also reporting lower satisfaction and higher risk.
    - Compared infrastructure quality against patient load and staff ratios to highlight where service delivery is most at risk.

- **Visualization:**  
  - Generated summary charts: bar plots, score distributions, condition ratings  
  - Each visual was used to identify and prioritize facilities needing attention

### 🧮 Predictive Modeling

- **Techniques:**  
  Classification models predict whether renovation is needed or not, categorizing facilities accordingly.

- **Key Features:**  
  Age score, restroom condition, electricity and heating quality, fire safety, and staff-per-visitor ratio.

- **Labels Assigned:**  
  - ✅ Ideal  
  - ⚠️ Acceptable  
  - ❌ Needs Review  

- **Impact:**  
  Highlights high-risk hospitals and prioritizes upgrades based on infrastructure and service gaps.

---


### 💡 Key Insights & Impact

- **Aging Facilities:** Many hospitals are outdated with poor infrastructure scores.
- **Utility & Safety Gaps:** Frequent lack of backup power, heating, and fire safety systems.
- **Sanitation Issues:** Weak restroom facilities and water supply remain common.
- **Staffing Pressure:** Rural hospitals often face staff shortages relative to patient load.


### 🚀 Future Opportunities: LLMs & GPT for Human Interaction
- GPT queries: “Show hospitals with no emergency room and built before 1990”
- Auto-reporting for ministry-level dashboards
- Chatbot support for healthcare administrators

### ⏭️ Next Steps
- Build predictive renovation index for healthcare facilities.
- Collaborate with local governments for risk-based funding allocation.

### 📌 Conclusion
This section supports hospital infrastructure planning using predictive analytics and AI to drive smart healthcare upgrades.

---

### 💻 For full technical details, see the Jupyter notebooks in this repository.
