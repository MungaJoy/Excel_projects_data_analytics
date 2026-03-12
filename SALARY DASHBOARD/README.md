 ## Introduction
 This Salary Dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are adequately compensated.
 The data used fo the analysis contains detailes information of job titles,salaries and location.  

  ![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/9614092f-d10b-47be-97d7-0f6af7426f68)

### My salary Dashboard
 You can find my final file here [SALARY_DASHBOARD (2).xlsx](SALARY_DASHBOARD(2).xlsx).

### Excel skills applied
The following excel skills were utilized for analysis  
-  📉Charts  
- 🧮Formulas and Functions  
-  ❎Data Validation

  ## Dashboard Build
  #### 📉Charts
  #### 📊 Data Science Job Salaries - Bar Chart
    
  <img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/3e0a552b-dff1-4bba-b210-e171e5c45458" />  
  

🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.  
🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.  
📉 Data Organization: Sorted job titles by descending salary for improved readability.  
💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles  

   ####  🗺️ Country Median Salaries - Map Chart
   
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/4615842c-8374-4cc5-9ff1-a46b6eb9eaa7)

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

  ### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table  

<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/4ceb54ef-11ed-4d15-9ee7-8f20717daf57" />

📉 Dashboard Implementation  

<img width="942" height="1212" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/95c97221-5ce7-47aa-8179-e2305ef4c923" />

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table  

<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/a0117850-0dce-427c-8fd6-ff3ea1810294" />

📉 Dashboard Implementation:

<img width="425" height="400" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/b122bfd3-b02e-46de-ab0d-bb37c6ff539b" />

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

<img width="1148" height="1214" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/454d01b6-9df6-4e1f-bbe2-6ed1a8787efb" />

## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 


