### Metadata for Employee and Project Datasets  

Metadata provides additional information about the structure, contents, and origin of the datasets. This metadata can be used to understand the datasets better, ensure data governance, and document the project for stakeholders.  

---

#### **Employee Dataset (`employee_data.csv`)**  

| **Metadata Attribute**       | **Details**                                                                                          |
|-------------------------------|------------------------------------------------------------------------------------------------------|
| **Dataset Name**             | Employee Dataset                                                                                   |
| **Description**              | Contains employee-specific information, including skills, training, and job details.               |
| **Source**                   | Generated synthetically for this project.                                                         |
| **File Format**              | CSV                                                                                               |
| **Number of Records**        | 500                                                                                               |
| **Number of Columns**        | 10                                                                                                |
| **Key Identifier**           | `Employee_ID`                                                                                     |
| **Column Names**             | `Employee_ID`, `Department`, `Job Role`, `Current Skills`, `Tenure (Years)`, `Certification History`, `Training Programs Attended`, `Skill Ratings`, `Promotion History`, `Retention Status`, `Assigned Project_ID` |
| **Update Frequency**         | Static (no updates).                                                                              |
| **Missing Data Handling**    | N/A (no missing values in this synthetic dataset).                                                |

---

#### **Project Dataset (`project_data.csv`)**  

| **Metadata Attribute**       | **Details**                                                                                          |
|-------------------------------|------------------------------------------------------------------------------------------------------|
| **Dataset Name**             | Project Dataset                                                                                    |
| **Description**              | Contains information on projects, including complexity, skills required, and team composition.     |
| **Source**                   | Generated synthetically for this project.                                                         |
| **File Format**              | CSV                                                                                               |
| **Number of Records**        | 250                                                                                               |
| **Number of Columns**        | 5                                                                                                |
| **Key Identifier**           | `Project_ID`                                                                                      |
| **Column Names**             | `Project_ID`, `Complexity`, `Required Skills`, `Team Composition`, `Future Skill Forecasts`        |
| **Update Frequency**         | Static (no updates).                                                                              |
| **Missing Data Handling**    | N/A (no missing values in this synthetic dataset).                                                |

---

#### **Combined Dataset (`combined_data.csv`)**  

| **Metadata Attribute**       | **Details**                                                                                          |
|-------------------------------|------------------------------------------------------------------------------------------------------|
| **Dataset Name**             | Combined Dataset                                                                                   |
| **Description**              | Merged dataset linking employee and project information.                                           |
| **Source**                   | Created by merging `employee_data.csv` and `project_data.csv`.                                     |
| **File Format**              | CSV                                                                                               |
| **Number of Records**        | 500                                                                                               |
| **Number of Columns**        | 15                                                                                                |
| **Key Identifiers**          | `Employee_ID`, `Assigned Project_ID`                                                              |
| **Column Names**             | `Employee_ID`, `Department`, `Job Role`, `Current Skills`, `Tenure (Years)`, `Certification History`, `Training Programs Attended`, `Skill Ratings`, `Promotion History`, `Retention Status`, `Assigned Project_ID`, `Project_ID`, `Complexity`, `Required Skills`, `Team Composition`, `Future Skill Forecasts` |
| **Join Criteria**            | Employee dataset is joined with the project dataset using `Assigned Project_ID` and `Project_ID`. |
| **Update Frequency**         | Static (no updates).                                                                              |
| **Missing Data Handling**    | N/A (no missing values in this synthetic dataset).                                                |

---

### Additional Notes  
1. **Purpose**:
   - These datasets simulate real-world HR and project management data, useful for machine learning, exploratory data analysis, and business intelligence tasks.  
2. **Synthetic Data**:
   - All data is generated synthetically, ensuring no privacy concerns.  
3. **Consistency**:
   - Fields like `Employee_ID` and `Assigned Project_ID` ensure consistent joins between datasets.  
4. **Intended Use**:
   - Ideal for modeling employee retention, skill gap analysis, and project team optimization.  

This metadata serves as documentation for stakeholders and ensures proper understanding and handling of the datasets.
