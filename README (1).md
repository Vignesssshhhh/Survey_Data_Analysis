# survey-data-analytics-azure-powerbi

**Survey Data Analytics System using Azure Cloud and Power BI**

---


## Introduction

Employee survey analytics is a critical aspect of modern organizations as it reflects workforce engagement, well-being, and organizational health. Traditional survey systems often lack the analytical depth needed to surface meaningful patterns across demographics. This project introduces a cloud-based survey analytics platform that integrates Microsoft Azure SQL Database for structured data storage, Azure Data Factory for data ingestion and transformation, Azure Blob Storage for raw data landing, and Power BI for generating interactive multi-visual dashboards. The system allows organizations to monitor workforce patterns and identify correlations between attributes such as education level, commute habits, marital status, and stress levels. By utilizing cloud technology and business intelligence tools, the project demonstrates how survey data can be transformed into actionable organizational insights.

---

## Project Overview

This project implements a cloud-based data analytics pipeline using Azure services and Power BI.

**Workflow:**

```
Dataset → Azure Blob Storage → Azure Data Factory (ETL) → Azure SQL Database → Power BI Dashboard → Analytical Insights
```

**Main Components:**

- Dataset containing employee survey responses
- Azure Storage Account (`surveydatasea2026`) for raw data landing
- Azure Data Factory (`surveyanalyticsdf`) for ETL pipeline orchestration
- Azure SQL Server (`survey-analytics-server`) for cloud database management
- Azure SQL Database (`free-sql-db-4219034`) for storing structured survey data
- Power BI dashboards for visualization and analytics

**The system analyzes different attributes including:**

- Department (IT, Finance, Operations, Marketing, Sales, Legal, Customer Service, HR)
- Education Level
- Gender
- Commute Mode (Bike, Car, Motorbike, Public Transport)
- Marital Status (Married, Single, Divorced, Widowed)
- Age and Experience
- Number of Companies worked at
- Number of Direct Reports
- Team Size
- Stress Levels
- Training Hours Per Year
- Physical Activity Hours
- Sleep Hours

---

## System Architecture

```
Data Source (CSV Dataset)
        ↓
Azure Blob Storage (Raw Data Layer)
        ↓
Azure Data Factory (ETL Pipeline)
        ↓
Azure SQL Database (Cloud Storage Layer)
        ↓
Power BI Desktop
        ↓
Interactive Analytics Dashboard
```

---

## Implementation Steps

### Step 1 — Azure Resource Group Creation

![Azure Resource Group](screenshots/azure_resource_group.png)<img width="1918" height="972" alt="Screenshot 2026-04-23 185018" src="https://github.com/user-attachments/assets/a50b56e2-d664-4bdf-a155-d8fd8168e553" />


This image shows the creation of the Azure Resource Group named `survey-analytics-rg` in the Microsoft Azure portal. The resource group is deployed in the **South India** region and acts as a container that organizes all cloud resources related to the project. It contains 4 resources: the Azure SQL Server, SQL Database, Data Factory, and Storage Account — all deployed in Southeast Asia. The deployment shows **3 Succeeded** deployments, confirming a successful cloud setup.

---

### Step 2 — Azure SQL Server and Database Setup

The Azure SQL Server (`survey-analytics-server`) and SQL Database (`free-sql-db-4219034`) were deployed within the resource group. The SQL Server manages database connections, authentication, and security, while the database stores the structured employee survey dataset. This setup enables scalable, cloud-based data storage and management accessible to Power BI via direct query.

---

### Step 3 — Azure Storage Account and Data Factory Setup

The Azure Storage Account (`surveydatasea2026`) serves as the raw data landing zone where the survey CSV file is uploaded initially. The Azure Data Factory (`surveyanalyticsdf`) is configured with a pipeline that reads data from Blob Storage, applies transformations, and loads it into the Azure SQL Database — completing the ETL (Extract, Transform, Load) workflow.

---

### Step 4 — Database Table Creation in Azure SQL

SQL scripts were executed in the Azure SQL Query Editor to create tables with columns representing all survey attributes such as `EmpID`, `Dept`, `EduLevel`, `Gender`, `Age`, `Experience`, `CommuteMode`, `MaritalStatus`, `NumCompanies`, `NumReports`, `TeamSize`, `Stress`, `TrainingHoursPerYear`, `PhysicalActivityHours`, and `SleepHours`. This structure enables efficient storage and complex querying of the survey dataset.

---

### Step 5 — Power BI Dashboard Visualization

![Power BI Dashboard](screenshots/powerbi_dashboard.png)<img width="1417" height="792" alt="Execution ScreenShot" src="https://github.com/user-attachments/assets/86f3c604-ecc5-4ec6-8c69-88b3bb0c43db" />



This screenshot shows the Power BI dashboard connected to the Azure SQL Database. The dashboard includes three main visualizations:

1. **Donut Chart — Count of EmpID and Sum of Experience by Dept and EduLevel**: Shows the distribution of employees and their collective experience across departments (IT leads with 594 employees at 19.64%), broken down by education level.

2. **Small Multiple Line Charts — Sum of Age, NumReports, TeamSize, Stress, and TrainingHoursPerYear by Gender and CommuteMode**: Shows how key metrics vary across Gender (Female, Male, Other) for each commute mode (Bike, Car, Motorbike, Public Transport).

3. **Clustered Bar Chart — Sum of NumCompanies, NumReports, PhysicalActivityHours, and SleepHours by MaritalStatus**: Compares multiple lifestyle and career metrics across marital status categories (Married, Single, Divorced, Widowed).

Power BI retrieves data directly from the Azure SQL cloud database, enabling real-time refreshes.

---

## Technologies Used

| Technology | Purpose |
|---|---|
| Microsoft Azure | Cloud Platform |
| Azure SQL Server | Database Server Management |
| Azure SQL Database | Structured Data Storage |
| Azure Data Factory | ETL Pipeline Orchestration |
| Azure Blob Storage | Raw Data Landing Zone |
| Power BI Desktop | Data Visualization & Analytics |
| SQL | Data Definition and Querying |
| GitHub | Version Control & Project Hosting |

---

## Key Insights from Analysis

- **IT Department Dominates**: IT is the largest department with 594 employees (19.64%), followed by Finance and Operations, indicating a technology-heavy workforce.
- **Commute Mode Influences Stress**: Car commuters show notably higher stress and team size values compared to bike or motorbike users, suggesting traffic-related work pressure.
- **Married Employees Work at More Companies**: Married employees show the highest sum of NumCompanies and SleepHours, reflecting longer career spans and more settled lifestyles.
- **Gender Patterns in Training**: Male employees show slightly higher TrainingHoursPerYear across most commute modes, indicating potential gender gaps in training opportunities.
- **Divorced Employees Show Lower Engagement Metrics**: Across NumReports, PhysicalActivityHours, and SleepHours, divorced employees show comparatively lower values, which may indicate work-life imbalance.
- **Public Transport Users Have Higher Stress**: Compared to other commute modes, public transport users show elevated stress and age metrics, suggesting longer commutes are a contributing factor.

---

## Conclusion

The Survey Data Analytics System demonstrates how cloud computing and business intelligence tools can be used to analyze workforce survey data effectively. By integrating Azure Blob Storage, Azure Data Factory, Azure SQL Database, and Power BI dashboards, the system provides a complete end-to-end analytics pipeline from raw data to actionable insights. The project highlights the importance of data-driven decision-making in HR and organizational management, and showcases the potential of cloud-based ETL and analytics platforms in transforming raw survey responses into meaningful workforce intelligence.

---

## Project Files

| File | Description |
|---|---|
| `Cloud Survey Analytics Azure (1).pptx` | Project presentation slide deck |
| `Project_Abstract.docx` | Project abstract document |
| `Cloud_Survey_Analytics_Azure.docx` | Detailed project report document |
| `employee_survey.csv` | Raw employee survey dataset |
| `Execution ScreenShot.png` | Azure portal and Power BI dashboard screenshots |
| `README.md` | Project documentation |

**Cloud Platform:** Microsoft Azure  
**Database:** Azure SQL Database  
**ETL Tool:** Azure Data Factory  
**Visualization Tool:** Power BI Desktop  

---

## About

Survey Data Analytics System using Azure Cloud Services and Power BI — analyzing employee workforce survey data to uncover patterns in department distribution, commute behavior, stress levels, and lifestyle metrics.
