# **Banking System**

## Task requirements:
**Scenario:** 
A bank needs a system to manage customer accounts, employees, loans, and transactions. 
1. Requirements: 
   - The bank operates multiple branches, each with a branch ID, address, and phone number. 
   - Customers can have multiple accounts, but each account belongs to only one customer. 
   - Customers are identified by a customer ID, name, address, phone number, and date of birth. 
   - Each account has an account number, balance, type (savings/checking), and date of creation. 
   - Each account can have multiple transactions (withdrawals, deposits, transfers), each with a unique 
     transaction ID, date, amount, and type. 
   - Loans are provided to customers, with each loan having an ID, type, amount, and issue date. 
   - A customer can have multiple loans, but each loan is handled by a specific employee. 
   - Employees are identified by employee ID, name, position, and branch ID (they work in one branch). 
   - Employees may assist customers in opening accounts or processing loans (relationship attribute: 
     action_type). 

## Task ERD and Mapping:

![Banking System ERD and Mapping](../image/Task4BankingSystem.png)

![Banking System Normaliztion](../image/BankSystemNormaliztion.png)

**1. First Normal Form (1NF) Solution:**
|CustomerID |CustomerName |Branch |RelationshipManager |
|-----------|-------------|-------|--------------------|
|C001       |Latifa       |Seeb   |Mr. Jamal           |
|C002       |Khalid       |Mutrah |Ms. Huda            |
|C003       |Rania        |Seeb   |Mr. Jamal           |


|CustomerID |AccountsID |Accounts Type |
|-----------|-----------|--------------|
|C001       |A001       |Savings       |
|C001       |A002       |Credit        |
|C002       |A003       |Current       |
|C003       |A004       |Savings       |
|C003       |A005       |Loan          |
|C003       |A006       |Card          |


--------------------------------------------------------------------------
**2. Second Normal Form (2NF)  Solution:**
|CustomerID |CustomerName |Branch |RelationshipManager |
|-----------|-------------|-------|--------------------|
|C001       |Latifa       |Seeb   |Mr. Jamal           |
|C002       |Khalid       |Mutrah |Ms. Huda            |
|C003       |Rania        |Seeb   |Mr. Jamal           |


|AccountsID |Accounts Type |
|-----------|--------------|
|A001       |Savings       |
|A002       |Credit        |
|A003       |Current       |
|A004       |Savings       |
|A005       |Loan          |
|A006       |Card          |

|CustomerID |AccountsID |
|-----------|-----------|
|C001       |A001       |
|C001       |A002       |
|C002       |A003       |
|C003       |A004       |
|C003       |A005       |
|C003       |A006       |