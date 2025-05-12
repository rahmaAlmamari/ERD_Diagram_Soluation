# **De-Normalization**

## 1. What is denormalization and how does it work?

Denormalization is the process of adding precomputed redundant data to an otherwise normalized relational database to improve read performance. With denormalization, the database administrator selectively adds back specific instances of redundant data after the data structure has been normalized.

![Denormaliztion](../image/Denormalization.png)

## 2. How is Denormalization Different From Normalization ?

Normalization and Denormalization both are the method which use in database but it works opposite to each other. One side normalization is used for reduce or removing the redundancy which means there will be no duplicate data or entries in the same table and also optimizes for data integrity and efficient storage, while Denormalization is used for add the redundancy into normalized table so that enhance the functionality and minimize the running time of database queries (like joins operation ) and optimizes for performance and query simplicity.

In a system that demands scalability, like that of any major tech company, we almost always use elements of both normalized and denormalized databases.

## 3. Advantages of Denormalization

 - **Improved Query Performance:** Denormalization can improve query performance by reducing the number of joins required to retrieve data.
 - **Reduced Complexity:** By combining related data into fewer tables, denormalization can simplify the database schema and make it easier to manage.
 - **Easier Maintenance and Updates:** Denormalization can make it easier to update and maintain the database by reducing the number of tables.
 - **Improved Read Performance:** Denormalization can improve read performance by making it easier to access data.
 - **Better Scalability:** Denormalization can improve the scalability of a database system by reducing the number of tables and improving the overall performance.

 ## 4. Disadvantages of Denormalization

 - **Reduced Data Integrity:** By adding redundant data, denormalization can reduce data integrity and increase the risk of inconsistencies.
 - **Increased Complexity:** While denormalization can simplify the database schema in some cases, it can also increase complexity by introducing redundant data.
 - **Increased Storage Requirements:** By adding redundant data, denormalization can increase storage requirements and increase the cost of maintaining the database.
 - **Increased Update and Maintenance Complexity:** Denormalization can increase the complexity of updating and maintaining the database by introducing redundant data.
 - **Limited Flexibility:** Denormalization can reduce the flexibility of a database system by introducing redundant data and making it harder to modify the schema.

