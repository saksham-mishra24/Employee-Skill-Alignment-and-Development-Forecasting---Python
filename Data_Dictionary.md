### Data Dictionary for Employee and Project Datasets  

This data dictionary provides detailed descriptions of all attributes in the **Employee** and **Project** datasets, including data types, possible values, and their role in the analysis.  

---

#### **Employee Dataset (`employee_data.csv`)**  
This dataset contains employee-specific information, including their department, skills, training history, and assigned project.  

| **Column Name**              | **Description**                                                                                           | **Data Type** | **Possible Values / Examples**                                             |
|-------------------------------|-----------------------------------------------------------------------------------------------------------|---------------|-----------------------------------------------------------------------------|
| `Employee_ID`                | Unique identifier for each employee.                                                                     | String        | `EMP0001`, `EMP0450`                                                       |
| `Department`                 | Department where the employee works.                                                                     | String        | `IT`, `HR`, `Finance`, `Operations`, `R&D`                                 |
| `Job Role`                   | Specific role or title of the employee.                                                                  | String        | `Data Analyst`, `Software Engineer`, `Project Manager`, `Business Analyst` |
| `Current Skills`             | List of current skills possessed by the employee, separated by commas.                                   | String        | `Python, SQL`, `Excel, Data Analysis`                                      |
| `Tenure (Years)`             | Number of years the employee has been with the company.                                                  | Integer       | `1` to `15`                                                                |
| `Certification History`      | Certifications obtained by the employee, if any.                                                         | String        | `Certified Data Scientist`, `PMP`, `AWS Certified`, `None`                 |
| `Training Programs Attended` | Number of training programs the employee has attended.                                                   | Integer       | `0` to `10`                                                                |
| `Skill Ratings`              | Average skill rating of the employee on a scale of 1 to 5.                                               | Float         | `1.00`, `3.75`, `4.50`                                                     |
| `Promotion History`          | Total number of promotions the employee has received.                                                    | Integer       | `0` to `3`                                                                 |
| `Retention Status`           | Current employment status of the employee.                                                              | String        | `Retained`, `Left`                                                         |
| `Assigned Project_ID`        | Project ID the employee is assigned to, linking to the project dataset.                                  | String        | `PROJ001`, `PROJ050`                                                       |

---

#### **Project Dataset (`project_data.csv`)**  
This dataset contains project-specific information, such as complexity, required skills, and future skill forecasts.  

| **Column Name**          | **Description**                                                                                          | **Data Type** | **Possible Values / Examples**                         |
|---------------------------|----------------------------------------------------------------------------------------------------------|---------------|-------------------------------------------------------|
| `Project_ID`             | Unique identifier for each project.                                                                     | String        | `PROJ001`, `PROJ025`                                  |
| `Complexity`             | Level of complexity associated with the project.                                                        | String        | `Low`, `Medium`, `High`                               |
| `Required Skills`        | List of skills required to successfully complete the project, separated by commas.                       | String        | `Python, Data Analysis`, `Project Management, SQL`    |
| `Team Composition`       | Number of team members working on the project.                                                          | Integer       | `3` to `10`                                           |
| `Future Skill Forecasts` | Skills anticipated to be critical for the project in the future, separated by commas.                    | String        | `Machine Learning, Python`, `SQL, Cloud Computing`    |

---

#### **Combined Dataset (`combined_data.csv`)**  
This dataset merges the `employee_data` and `project_data` datasets, allowing for in-depth analysis of employee-project relationships.  

| **Column Name**              | **Description**                                                                                      | **Source**         |
|-------------------------------|------------------------------------------------------------------------------------------------------|--------------------|
| `Employee_ID`                | Unique identifier for each employee.                                                                | Employee Dataset   |
| `Department`                 | Department where the employee works.                                                                | Employee Dataset   |
| `Job Role`                   | Specific role or title of the employee.                                                             | Employee Dataset   |
| `Current Skills`             | List of current skills possessed by the employee, separated by commas.                              | Employee Dataset   |
| `Tenure (Years)`             | Number of years the employee has been with the company.                                             | Employee Dataset   |
| `Certification History`      | Certifications obtained by the employee, if any.                                                    | Employee Dataset   |
| `Training Programs Attended` | Number of training programs the employee has attended.                                              | Employee Dataset   |
| `Skill Ratings`              | Average skill rating of the employee on a scale of 1 to 5.                                          | Employee Dataset   |
| `Promotion History`          | Total number of promotions the employee has received.                                               | Employee Dataset   |
| `Retention Status`           | Current employment status of the employee.                                                         | Employee Dataset   |
| `Assigned Project_ID`        | Project ID the employee is assigned to. Links to `Project_ID` in the project dataset.               | Employee Dataset   |
| `Project_ID`                 | Unique identifier for each project.                                                                | Project Dataset    |
| `Complexity`                 | Level of complexity associated with the project.                                                   | Project Dataset    |
| `Required Skills`            | List of skills required to successfully complete the project, separated by commas.                 | Project Dataset    |
| `Team Composition`           | Number of team members working on the project.                                                     | Project Dataset    |
| `Future Skill Forecasts`     | Skills anticipated to be critical for the project in the future, separated by commas.               | Project Dataset    |

---

### How to Use the Dictionary  
1. **EDA and Data Cleaning**:
   - Use the dictionary to understand each column's purpose and ensure data consistency during preprocessing.
2. **Joining Data**:
   - Use `Employee_ID` and `Assigned Project_ID` to join datasets seamlessly.
3. **Feature Engineering**:
   - Extract valuable insights, such as the gap between `Current Skills` and `Required Skills`.
4. **Analysis and Reporting**:
   - Leverage attributes like `Skill Ratings`, `Complexity`, and `Team Composition` for detailed performance analysis.

This dictionary ensures clarity while working on the project, particularly during EDA and feature engineering stages.
