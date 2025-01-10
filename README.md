# Business Analyst | Data Analyst | BI-specialist
**Technical Skills:** MS Office, Power BI & Tableau, SQL, Python, MATLAB, MS Dynamics 365.
[View Russian version.]()
## Contacts:
Email: ssur.tot@gmail.com

[LinkedIn](https://www.linkedin.com/in/anastasiya-lukyanava-642954344/)
## Education
**Belarusian State Economic University** - «Economic cybernetics» | 2021 - 2025

Bachelor’s Degree

**IT Academy** - «Business Analysis in Software Development» | Sep 2024 - Dec 2024

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

#Images: diagrams, prototype fragments, and benchmarking table.
#Description: brief text under each element.

### 2 Bank data analysis and metrics visualization | Nov 2024
---
**Done:** 7 SQL queries, 3 Power BI dashboards
#### Description:
The project focuses on the analysis and visualization of data related to banking activities. It includes the development of SQL queries for data processing and the creation of analytical dashboards. The main emphasis is on studying customer activity, revenue by city, purchase structure, repeat customers, and campaign effectiveness. The data is presented through interactive dashboards that enable filtering by cities, years, and other metrics for detailed analysis. The project is aimed at developing tools that facilitate informed decision-making in customer relationship management and business process optimization.

### 3 Road Traffic Accident Analytics | June 2024
---
#### Description:
This dashboard was created to analyze and monitor road traffic accident (RTA) statistics. It provides detailed information on the number of casualties, the nature of accidents, types of vehicles involved, road conditions, and other key metrics. The data used allows for the identification of critical factors affecting road safety and supports decision-making to reduce accident rates.

### 4 Stock Analysis Dashboard Using Streamlit | Nov 2023
---
#### Description:
The project involved developing a stock analytics dashboard using Python and the Streamlit library. The dashboard provides an interactive and user-friendly interface, featuring a collapsible sidebar with filters for company name, stock ticker, and year. The main section showcases a table with annual stock data, alongside visualizations such as charts and a calculated performance coefficient. This tool offers a streamlined approach to exploring stock data and supports informed investment decisions.

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

- **Jacobi Rotation Function (`JA_COBI`):**  
   Implements the iterative Jacobi algorithm.  
```matlab
function [A, eigenVectorMatrix, k] = JA_COBI(A)
[row, col] = size(A);
eigenVectorMatrix = eye(row, col);
k = 0;

while(~isDiagonal(A))
    phi = findPhi(A);
    [largest, row_ind, col_ind] = findLargestElement(A);
    T = eye(row, col);
    T(row_ind, row_ind) = cos(phi);
    T(row_ind, col_ind) = sin(phi);
    T(col_ind, row_ind) = -sin(phi);
    T(col_ind, col_ind) = cos(phi);
    A = T' * A * T;
    eigenVectorMatrix = eigenVectorMatrix * T;
    k = k + 1;
end
end
```

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
