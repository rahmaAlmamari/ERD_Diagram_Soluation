#  **Airline Information System**

## Task requirements:
An airline system is needed to manage flight operations, schedules, reservations, and related data: 

1. AIRPORT 
  - Each airport has a unique airport_code. 
  - It stores city, state, and name. 
  - An airport can serve as a departure or arrival point for many flight legs. 
  - An airport may allow landing of different airplane types. 
	
2. FLIGHT LEG 
   - Each flight leg is uniquely identified by a leg_no. 
   - A leg has a scheduled_dep_time and scheduled_arr_time. 
   - A leg departs from and arrives at an airport. 
   
3. LEG INSTANCE 
   - A leg instance is a specific occurrence of a flight leg on a given date. 
   - It includes: 
      - Arrival time 
      - Departure time 
      - Number of available seats 
   - It is assigned an airplane and connected to seat reservations. 
   
4. AIRPLANE TYPE 
   - Defined by a type_name, company, and max_seats. 
   - Multiple airplanes can share a type. 
   
5. AIRPLANE 
   - Identified by airplane_id. 
   - Has a total number of seats. 
   - Each airplane belongs to a specific type. 
   - Assigned to leg instances. 
   
6. SEAT / RESERVATION 
   - A reservation is made by a customer with name and phone. 
   - It is linked to a specific seat number in a leg instance. 
   
7. FLIGHT & FARE 
   - A flight includes multiple legs. 
   - Flights have attributes like: 
     - Airline 
     - Weekdays 
     - Restrictions 
   - Each flight can have multiple fares, with: 
     - Code 
     - Amount 
     
## Task ERD:

![Airline Information System ERD](../image/AirlineInformationSystem.png)

## Task Mapping:

![Airline Information System Mapping](../image/AirlineInformationSystem-mapping.png)

## Task Normaliztion:

![Airline Information System Normaliztion](../image/AirlineNormaliztion.png)

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