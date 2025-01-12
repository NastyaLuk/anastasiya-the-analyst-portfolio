# Business Analyst | Data Analyst | BI-specialist
**Technical Skills:** MS Office, Power BI & Tableau, SQL, Python, MATLAB, MS Dynamics 365.

[View Russian version.](https://nastyaluk.github.io/anastasiya-the-analyst-portfolio-rus/)
## Contacts:
Email: ssur.tot@gmail.com

[LinkedIn](https://www.linkedin.com/in/anastasiya-lukyanava-642954344/)
## Education
**Belarusian State Economic University** - «Economic cybernetics» | 2021 - 2025

Bachelor’s Degree

**IT Academy** - «Business Analysis in Software Development»

Project - NFTeam: Project Management System with Gamification

## Work Experience

### НаучСофт | CRM-system Consultant | Internship
August 2024 - September 2024

1. Gained hands-on experience with MS Dynamics 365 CRM, including configuring and working with key modules such as Sales and Customer Service. 
2. Explored the integration and customization of workflows using Power Apps and Power Automate to streamline business processes. 
3. Developed a solid foundation in CRM system configuration and its practical application to enhance customer relationship management.

### IT Academy | Business Analyst | Internship
September 2024 - December 2024

### SoftClub | Support Specialist | Internship
January 2025 - Present

## Projects
All interface elements are presented in Russian.
### 1 NFTeam: Project Management System with Gamification | Nov 2024 - Dec 2024
---
#### Description:
Development of a project management system featuring task planning, analytical report generation, and unique gamification tools such as NFT avatars and progress visualization through a virtual city.

**Role:** Business Analyst
#### Key Responsibilities:
1. Collecting and analyzing requirements.
2. Preparing Vision & Scope and SRS documents.
3. Creating diagrams (Use case, Activity, context diagram).
4. Developing an interface prototype (Axure RP).
5. Conducting competitive analysis.
#### Project Outcomes:
1. SWOT analysis and benchmarking.
2. Vision & Scope and SRS documents.
3. Diagrams and interface prototype.

**Tools Used:** Mindmup, Draw.io, Axure RP, Google Docs.
#### Visuals:
**Use Case diagram**
![Use Case Diagram_NFTeam](/1.png)
**Profile view**
![Profile_NFTeam](/2.png)
**Tasks view**
![Tasks_NFTeam](/3.png)

### 2 Bank data analysis and metrics visualization | Nov 2024
---
**Done:** 7 SQL queries, 3 Power BI dashboards
#### Description:
The project focuses on the analysis and visualization of data related to banking activities. It includes the development of SQL queries for data processing and the creation of analytical dashboards. The main emphasis is on studying customer activity, revenue by city, purchase structure, repeat customers, and campaign effectiveness. The data is presented through interactive dashboards that enable filtering by cities, years, and other metrics for detailed analysis. The project is aimed at developing tools that facilitate informed decision-making in customer relationship management and business process optimization.

#### SQL Query for Clients with Multiple Loans in September 2023

#### **Objective**  
Retrieve detailed information for corporate clients (ЮЛ) who opened more than one loan agreement in September 2023. The output should include:  
1. Loan numbers (`num_loan`) for each client.  
2. Remaining balance (principal + overdue) for each loan as of 30.09.2023 (`rest_eq_loan`).  
3. Total remaining balance for all loans of the client (`rest_eq_client`).  

#### Input Data 
1. **LOANS**: Contains loan agreements with SCD Type 2 implementation. Active rows are identified by `dt_end = '3001-01-01'`.  
2. **CLIENTS**: Stores client details, also using SCD Type 2. Active clients have `dt_end = '3001-01-01'`.  
3. **LOANS_FACT**: Holds daily loan balances, including principal (`rest_od_eq`) and overdue (`rest_pd_eq`) amounts in BYN equivalent.  

#### SQL Query

```sql
SELECT 
    ld.name_client, 
    ld.num_loan, 
    ld.rest_eq_loan, 
    cs.rest_eq_client
FROM (
        SELECT 
            c.name_client, 
            l.num_loan, 
            l.id_client,
            SUM(f.rest_od_eq + f.rest_pd_eq) AS rest_eq_loan
        FROM LOANS l
        INNER JOIN CLIENTS c ON l.id_client = c.id_client
        INNER JOIN LOANS_FACT f ON l.id_loan = f.id_loan
        WHERE c.type_client = 'ЮЛ'
            AND l.dt_open_loan BETWEEN '2023-09-01' AND '2023-09-30'
            AND f.dt = '2023-09-30'
            AND l.dt_end = '3001-01-01'
            AND c.dt_end = '3001-01-01'
        GROUP BY c.name_client, l.num_loan, l.id_client
    ) ld
INNER JOIN 
    (
        SELECT 
            c.name_client, 
            l.id_client, 
            SUM(f.rest_od_eq + f.rest_pd_eq) AS rest_eq_client
        FROM LOANS l
        INNER JOIN CLIENTS c ON l.id_client = c.id_client
        INNER JOIN LOANS_FACT f ON l.id_loan = f.id_loan
        WHERE c.type_client = 'ЮЛ'
            AND l.dt_open_loan BETWEEN '2023-09-01' AND '2023-09-30'
            AND f.dt = '2023-09-30'
            AND l.dt_end = '3001-01-01'
            AND c.dt_end = '3001-01-01'
        GROUP BY c.name_client, l.id_client
        HAVING COUNT(l.id_loan) > 1
    ) cs
ON ld.id_client = cs.id_client
ORDER BY ld.name_client;
```

#### Output Fields
- **`name_client`**: Name of the corporate client.  
- **`num_loan`**: Loan agreement number.  
- **`rest_eq_loan`**: Remaining balance (principal + overdue) for each loan as of 30.09.2023.  
- **`rest_eq_client`**: Total remaining balance for all loans of the client as of 30.09.2023.  

#### Dashboards:
![Bank_dashboard_1](/8.png)
![Bank_dashboard_2](/9.png)
![Bank_dashboard_2](/10.png)

### 3 Road Traffic Accident Analytics | June 2024
---
#### Description:
This dashboard was created to analyze and monitor road traffic accident (RTA) statistics. It provides detailed information on the number of casualties, the nature of accidents, types of vehicles involved, road conditions, and other key metrics. The data used allows for the identification of critical factors affecting road safety and supports decision-making to reduce accident rates.
![RTA_Analysis](/7.PNG)

### 4 Stock Analysis Dashboard Using Streamlit | Nov 2023
---
#### Description:
The project involved developing a stock analytics dashboard using Python and the Streamlit library. The dashboard provides an interactive and user-friendly interface, featuring a collapsible sidebar with filters for company name, stock ticker, and year. The main section showcases a table with annual stock data, alongside visualizations such as charts and a calculated performance coefficient. This tool offers a streamlined approach to exploring stock data and supports informed investment decisions.
![Stok_Analusis_1](/Crocs и S&P Global_1.PNG)
![Stok_Analusis_2](/Crocs и S&P Global_3.PNG)
![Stok_Analusis_3](/Crocs и S&P Global_2.PNG)

### 5 Jacobi rotation matrix on MATLAB | Apr 2023 - May 2023
---
#### Description:
The project explores the implementation of the Jacobi rotation method for solving the complete symmetric eigenvalue problem. The method, renowned for its simplicity and accuracy, is applied to calculate the eigenvalues and eigenvectors of symmetric matrices. The project involves developing a MATLAB program to demonstrate the algorithm's practical application, supported by examples and results.

#### Objectives: 
- To understand the theoretical foundations of the Jacobi rotation method.  
- To implement the algorithm in MATLAB for calculating eigenvalues and eigenvectors of symmetric matrices.  
- To apply the method to practical examples, including Markov chains in economic modeling.

#### Practical Implementation: 
The MATLAB implementation involves the following core functions:  

**Jacobi Rotation Function (`JA_COBI`):**  
   Implements the iterative Jacobi algorithm.  
![Jacobi_code](/13.png)

- Supporting Functions: 
   - `findPhi`: computes the rotation angle.  
   - `findLargestElement`: identifies the largest off-diagonal matrix element.  
   - `isDiagonal`: checks if a matrix is diagonal.

#### Highlights: 
- Algorithmic Implementation: developed a complete Jacobi rotation algorithm in MATLAB.  
- Economic Insight: applied eigenvalue computation to real-world Markov chain models.  
- Accuracy: verified results with MATLAB’s built-in functions, ensuring reliability.  
- Scalability: designed the program to handle various symmetric matrices and scenarios.

### 6 MMA Battle Simulator | Apr 2023 - May 2023
---
**Role:** Business Analyst

**Done:** Market analysis, benchmarking, Vision&Scope Document
#### Description:
**"MMA Battle Simulator"** is a desktop combat simulator with simplified gameplay. The project aims to create a minimum viable product (MVP) that demonstrates the basic mechanics of the game and the possibilities for future expansion.
#### Key Achievements:
1. Requirements Analysis: the needs of users and competitors were studied to form the functionality of the MVP.
2. Efficient Implementation: the basic gameplay with an optimized interface and performance was implemented.
3. Documentation: the requirements structure, functionality description and analog analysis were prepared.
4. Scalability: a flexible product with the ability to add new functions was designed.

### 7 Conscious consumption of cosmetic products: the choice of Belarusians | Apr 2022 - May 2022
---
#### Description:
Conducted a survey of over 200 respondents (205 women and 16 men) to analyze consumer behavior in the Belarusian skincare market. The study explored factors influencing product selection, such as natural ingredients, price, and brand reputation, as well as the role of sustainability in consumer preferences. Recommendations were developed for improving the competitiveness of Belarusian cosmetics through environmentally friendly ingredient selection and packaging. A detailed report with insights and recommendations on selected products was prepared, highlighting the growing trend of conscious consumption in Belarus.

[Publication](http://edoc.bseu.by:8080/handle/edoc/97163?locale=ru)

![Survey](/12.png)
![Content](/11.png)
