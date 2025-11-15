# 📌 **LinkedIn Job Posting Analysis (2023–2024)**

A complete end-to-end data analysis project based on **124,000+ LinkedIn job postings**, covering **job roles, skills, salaries, industries, locations, and companies**.
This project answers real HR, business, and data science questions and includes **salary prediction using Machine Learning**.

---

## 📁 **Project Structure**

```
LinkedIn_Job_Posting_Analysis/
│
├── data/                   # (Your datasets)
├── notebooks/              # Jupyter notebook(s)
├── models/                 # Saved ML models (.joblib / .pkl.gz)
├── README.md               # Project documentation
├── requirements.txt        # Python dependencies
```

---

# 🎯 **1. Project Objective**

The goal of this project is to analyze LinkedIn job postings and extract insights that are useful for:

* Job seekers
* HR teams
* Recruiters
* Companies
* Data science hiring analysts

The project covers:

* Understanding job demand trends
* Salary patterns
* Industry hiring behaviour
* Skill importance
* Remote vs onsite distribution
* Salary prediction using machine learning

---

# 📊 **2. Dataset Overview**

The project uses **11 CSV files** from a LinkedIn job dataset:

* `postings.csv`
* `skills.csv`
* `job_skills.csv`
* `industries.csv`
* `job_industries.csv`
* `companies.csv`
* `company_industries.csv`
* `company_specialities.csv`
* `salaries.csv`
* `benefits.csv`
* `employee_counts.csv`

Each table was joined using `job_id` and `company_id`.

---

# 🔧 **3. Data Cleaning & Preprocessing**

✔ Filled missing salary values (min, median, max)
✔ Merged salary info from two files
✔ Cleaned work type, skills, remote flags
✔ Removed duplicates
✔ Extracted industry names & skill names using JOIN operations
✔ Created final consolidated dataset for EDA & ML

---

# 📈 **4. Exploratory Data Analysis**

### ✅ **4.1 Most In-Demand Job Titles**

Top hiring roles:

* Sales Manager
* Receptionist
* Salesperson
* Customer Service Representative
* Project Manager
* Software Engineer
* Registered Nurse

---

### ✅ **4.2 Most Hiring Industries**

Industries with the highest job volume:

* Retail
* Healthcare
* IT
* Finance
* Manufacturing

---

### ✅ **4.3 Location Trends**

Cities with the highest job postings:

* New York
* Chicago
* Dallas
* Los Angeles
* Houston

---

### ✅ **4.4 Salary Insights**

Highest paying job categories:

* Engineering
* Data & AI roles
* Senior management
* Healthcare specialists

Lowest paying:

* Customer service
* Retail assistants

---

### ✅ **4.5 Skills Analysis**

Most demanded skills:

* Management
* Sales
* Customer Service
* Excel
* Project Management
* Python & SQL (tech roles)

---

### ✅ **4.6 Remote Job Insights**

* Only ~9% of jobs allow remote work
* Tech & Marketing have highest remote offerings

---

# 🤖 **5. Machine Learning — Salary Prediction**

A Random Forest Regressor was trained to predict job salary using:

### **Features Used**

* Job title (TF-IDF NLP vectors)
* Industry (OneHot encoded)
* Skills
* Company follower count
* Company employee size
* Remote allowed
* Min/Max/Median Salary fields

### **Model Performance**

```
RMSE: 13,415
R² Score: 0.92
```

A strong performance indicating the model explains **92% of salary variation**.

---

# 💾 **6. Model Saving**

The model was compressed and saved using:

```python
joblib.dump(rf_model_small, "rf_model_compressed.joblib", compress=('gzip', 9))
```

Resulting file size: **3–10 MB (GitHub-friendly)**.

---

# 📚 **7. Key Business Insights**

### ✔ High-demand roles are not always high-paying

### ✔ Tech & healthcare consistently lead in salaries

### ✔ Remote roles are still limited

### ✔ Management, Sales & Communication dominate skill demand

### ✔ Company size & follower count strongly influence salary

### ✔ Location significantly impacts compensation

---

# 🏆 **8. What This Project Demonstrates**

This project shows your ability to:

✔ Handle large multi-file datasets
✔ Merge relational data (SQL-style joins in pandas)
✔ Perform advanced EDA
✔ Clean and preprocess complex job market data
✔ Use NLP (TF-IDF) for text features
✔ Build a regression model with high accuracy
✔ Extract insights for business decision-making
✔ Write production-quality code & documentation

---

# 🚀 **9. Future Enhancements**

* Job recommendation system
* Skill gap analysis
* Time-series trend predictions
* Company growth predictors
* Full NLP analysis of job descriptions (BERT/LSTM)

---

# 💻 **10. How to Run the Project**

### Install dependencies

```
pip install -r requirements.txt
```

### Run notebook

Open:

```
notebooks/Linkedin_Job_Posting_Analysis.ipynb
```

---

# 🙌 **11. Author**

**Aliakbar Kanorewala**
Data Science & Machine Learning Enthusiast
Passionate about industry-focused analytics & practical ML solutions.


