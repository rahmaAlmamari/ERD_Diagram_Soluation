# **Company Database**

## Task requirements:
This system manages a company's departments, employees, projects, and their dependents: 

1. EMPLOYEE 
   - Identified by SSN. 
   - Attributes: Fname, Minit, Lname, Address, Sex, Bdate, Salary. 
   - Can: 
       - Work for a department with StartDate 
       - Supervise other employees 
       - Be supervised 
       - Work on projects with hours logged 
       - Manage departments 
       - Have dependents 

2. DEPENDENT 
   - Each dependent is related to one employee. 
   - Attributes: Name, Sex, Birthdate, Relationship. 

3. DEPARTMENT 
   - Identified by Name. 
   - Attributes: Number, Locations, NumberOfEmployees. 
   - A department: 
       - Controls multiple projects 
       - Is managed by an employee 

4. PROJECT 
   - Identified by Name and Number. 
   - Attributes: Location 
   - Employees work on projects, each with logged hours. 

## Task ERD:

![Company Database ERD](../image/CompanyDatabase.png)

## Task Mapping:

![Company Database Mapping](../image/ERD_Case_Study_mapping.png)

## Task Normaliztion:

![Company Database Normaliztion](../image/CompanySystemNormalization.png)

**1. First Normal Form (1NF) Solution:**
|EmployeeID |EmployeeName |Department |Manager     |
|-----------|-------------|-----------|------------|
|E001       |Ahmed        |IT         |Eng. Khalid |
|E002       |Salim        |HR         |Ms. Amal    |
|E003       |Aisha        |IT         |Eng. Khalid | 


|EmployeeID |ProjectsID |Projects Name    |
|-----------|-----------|-----------------|
|E001       |P101       |Website          |
|E001       |P102       |Mobile App       |
|E002       |P103       |Recruitment      |
|E003       |P102       |Mobile App       |
|E003       |P104       |Database Upgrade |

--------------------------------------------------------------------------
**2. Second Normal Form (2NF)  Solution:**
|EmployeeID |EmployeeName |Department |Manager     |
|-----------|-------------|-----------|------------|
|E001       |Ahmed        |IT         |Eng. Khalid |
|E002       |Salim        |HR         |Ms. Amal    |
|E003       |Aisha        |IT         |Eng. Khalid | 

|ProjectsID |Projects Name    |
|-----------|-----------------|
|P101       |Website          |
|P102       |Mobile App       |
|P103       |Recruitment      |
|P102       |Mobile App       |
|P104       |Database Upgrade |

|EmployeeID |ProjectsID |
|-----------|-----------|
|E001       |P101       |
|E001       |P102       |
|E002       |P103       |
|E003       |P102       |
|E003       |P104       |