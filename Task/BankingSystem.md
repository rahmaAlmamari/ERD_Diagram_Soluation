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

![College Management System ERD and Mapping](../image/Task4BankingSystem.png)