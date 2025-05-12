# **College Management System**

## Task requirements:
A college database system is needed to manage students, faculty, courses, hostels, and examinations: 

1. FACULTY 
   - Identified by F_id. 
   - Attributes: Name, Mobile_no, Department, Salary. 
   - Teaches multiple students and handles subjects. 

2. STUDENT 
   - Identified by S_id. 
   - Attributes: F_name, L_name, Name, Phone_no, DOB, and Age (derived). 
   - Can: 
     - Enroll in multiple courses 
     - Belong to a department 
     - Take multiple exams 
     - Live in a hostel 

3.  HOSTEL 
    - Identified by Hostel_id. 
    - Attributes: Hostel_name, City, State, Address, Pin_code, No_of_seats. 

4. COURSE 
    - Identified by Course_id. 
    - Attributes: Course-name, Duration. 
    - Courses are handled by departments and have multiple enrolled students. 

5. SUBJECT 
    - Each subject has a Subject_id and Subject_name. 
    - Students take subjects which are taught by faculty. 

6. EXAMS 
    - Identified by Exam_code. 
    - Attributes: Date, Time, Room. 
    - Conducted by a department. 

7. DEPARTMENT 
    - Identified by Department_id. 
    - Has a D_name. 
    - Handles courses and conducts exams.

## Task ERD:

![College Management System ERD](../image/CollegeManagementSystem.png)

## Task Mapping:

![College Management System Mapping](../image/CollegeManagementSystem-mapping.png)

## Task Normaliztion:

![College Management System Normaliztion](../image/CollegeNormaliztion.png)

**1. First Normal Form (1NF) Solution:**
|StudentID |StudentName |Department |Advisor   |
|----------|------------|-----------|----------|
|S001      |Reem        |CS         |Dr. Omar  |
|S002      |Tariq       |Business   |Dr. Sarah |
|S003      |Noura       |CS         |Dr. Omar  | 


|StudentID |CoursesID  |Courses Name  |
|----------|-----------|--------------|
|S001      |C101       |DB            |
|S001      |C102       |AI            |
|S002      |C103       |Marketing     |
|S003      |C101       |DB            |
|S003      |C104       |Cybersecurity |

--------------------------------------------------------------------------
**2. Second Normal Form (2NF)  Solution:**
|StudentID |StudentName |Department |Advisor   |
|----------|------------|-----------|----------|
|S001      |Reem        |CS         |Dr. Omar  |
|S002      |Tariq       |Business   |Dr. Sarah |
|S003      |Noura       |CS         |Dr. Omar  | 


|CoursesID  |Courses Name  |
|-----------|--------------|
|C101       |DB            |
|C102       |AI            |
|C103       |Marketing     |
|C101       |DB            |
|C104       |Cybersecurity |

|StudentID |CoursesID |
|----------|----------|
|S001      |C101      |
|S001      |C102      |
|S002      |C103      |
|S003      |C101      |
|S003      |C104      |