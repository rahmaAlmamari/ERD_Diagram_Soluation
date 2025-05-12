# **Hotel Management System**

## Task requirements:
**Scenario:** 
A hotel chain wants to develop a database system to manage its bookings, rooms, customers, and staff across 
multiple branches. 
1. Requirements: 
   - The hotel chain operates in multiple branches, each identified by a branch ID, name, and location. 
   - Each branch has multiple rooms, each identified by a room number, type, and nightly rate. 
   - A customer can book one or more rooms, and each booking includes a check-in and check-out date. 
   - A booking is linked to a customer and can include multiple rooms. 
   - Each customer has a unique ID, name, phone, and email. 
   - Staff are assigned to a specific branch and are identified by ID, name, job title, and salary. 
   - A staff member can check in or check out customers (many-to-many with role attribute like "check-in", 
     "check-out"). 
   - The system should track the availability of each room based on bookings. 

   
## Task ERD and Mapping:

![Hotel Management System ERD and Mapping](../image/Task4HotelManagementSystem.png)

## Task Normaliztion:

![Hotel Management System Normaliztion](../image/HotelNormaliztion.png)

**1. First Normal Form (1NF) Solution:**
|BookingID |PassengerName |PaymentMethod |
|----------|--------------|--------------|
|B001      |Salem         |Credit Card   |
|B002      |Fatma         |PayPal        |
|B003      |Zayed         |Credit Card   | 


|BookingID |FlightsID |From     |To       |
|----------|----------|---------|---------|
|B001      |F101      |Muscat   |Dubai    |
|B001      |F102      |Dubai    |London   |
|B002      |F103      |Muscat   |Istanbul |
|B003      |F104      |Istanbul |Paris    |
|B003      |F105      |Paris    |Oslo     |

|BookingID |FlightsID |SeatNumbers |
|----------|----------|------------|
|B001      |F101      |12A         |
|B001      |F102      |14C         |
|B002      |F103      |10B         |
|B003      |F104      |9A          |
|B003      |F105      |13A         |


--------------------------------------------------------------------------
**2. Second Normal Form (2NF)  Solution:**
|BookingID |PassengerName |PaymentMethod |
|----------|--------------|--------------|
|B001      |Salem         |Credit Card   |
|B002      |Fatma         |PayPal        |
|B003      |Zayed         |Credit Card   | 

|FlightsID |From     |To       |SeatNumbers |
|----------|---------|---------|------------|
|F101      |Muscat   |Dubai    |12A         |
|F102      |Dubai    |London   |14C         |
|F103      |Muscat   |Istanbul |10B         |
|F104      |Istanbul |Paris    |9A          |
|F105      |Paris    |Oslo     |13A         |

|BookingID |FlightsID |
|----------|----------|
|B001      |F101      |
|B001      |F102      |
|B002      |F103      |
|B003      |F104      |
|B003      |F105      |