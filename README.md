# MIS4610 Project 1
## Team Name:
24182 Group 2

## Team Members:
1. Andrew Macri 
2. Zach Schiller
3. Irene Jacob 
4. Alex Tumen
5. Fawazz Mohdraji

## Problem Description:
Modeling and developing a relational database for the whole operations of university student housing is the current goal. Each dorm represents a real residence hall or housing community run by the university, and it serves as the model's primary entity. The dorms function in conjunction with the rooms, students, employees, maintenance requests, payments, parking assignments, renovations, deliveries, and supply orders associated with housing operations. Accurately modeling these relationships, producing sample data, and using this sample data to populate the entities and their properties are our goals. In order to obtain useful business insights regarding university housing and its operations, we are also interested in running functional queries on this data.

## Data Model:
Our data model is based on the structure of a university housing system, where the central entity is the Dorm table. Each dorm represents a physical residence hall and contains attributes such as name, number of rooms, availability, number of floors, last renovation date, and dorm type. A dorm has a one-to-many relationship with Room, meaning each dorm contains multiple rooms.

The Room entity stores details about individual rooms, including size, number of beds, and room type. Each room is assigned to a Student, creating a one-to-one (or one-to-many over time) relationship between Room and Student. The Student entity contains student specific information such as name and email and serves as a key connection point in the model.

Students are connected to several operational aspects of housing. They can submit Maintenance requests, creating a one-to-many relationship where each student may have multiple requests. These requests track issues, request dates, statuses, and completion dates. Students are also linked to Payments, representing housing or parking payments, and to Parking, where each student may be assigned a parking permit.

The model also includes Employees, who are associated with dorms and departments. Each employee has a role (such as RA, maintenance, or staff) and is linked to a specific dorm, forming a one-to-many relationship between Dorm and Employees. Employees are further connected to the Department entity, which organizes staff into functional areas within the university.

Dorm operations are supported through logistics and upkeep entities. The Renovations entity tracks updates made to dorms, including areas renovated and completion timelines, forming a relationship with Dorm. The Deliveries entity represents supply deliveries made to dorms, which are linked to SupplyOrders that track order details such as number of items and total price.
Overall, this data model captures both the residential structure (dorms, rooms, students) and the operational processes (maintenance, payments, employees, logistics) of university housing. The relationships between these entities allow for efficient tracking, management, and querying of housing data to support administrative decision-making.

<img width="1270" height="1080" alt="image" src="https://github.com/user-attachments/assets/6b045017-1630-4ba1-ac54-5df58e152058" />


## Data Dictionary:
<img width="759" height="718" alt="Screenshot 2026-03-27 at 9 39 05 PM" src="https://github.com/user-attachments/assets/840333e4-3f54-4a61-aecf-636c6f433c2b" />
<img width="759" height="718" alt="Screenshot 2026-03-27 at 9 39 05 PM" src="https://github.com/user-attachments/assets/ddf2f420-cc1e-4e42-9204-0ff20b56dea8" />
<img width="769" height="954" alt="Screenshot 2026-03-27 at 9 39 32 PM" src="https://github.com/user-attachments/assets/e20af69b-3d42-438b-bf66-349bcff309a0" />
<img width="786" height="941" alt="Screenshot 2026-03-27 at 9 40 00 PM" src="https://github.com/user-attachments/assets/ef61c88a-9d2a-4596-955e-144521e48576" />
<img width="782" height="764" alt="Screenshot 2026-03-27 at 9 40 18 PM" src="https://github.com/user-attachments/assets/46489875-5334-40c9-b13f-4affae509a14" />
<img width="781" height="701" alt="Screenshot 2026-03-27 at 9 40 39 PM" src="https://github.com/user-attachments/assets/bad5bfce-5926-4502-b5ca-c3b8b4ebaaad" />
<img width="779" height="849" alt="Screenshot 2026-03-27 at 9 41 00 PM" src="https://github.com/user-attachments/assets/652809e3-0a56-4465-865b-5b03e0470de5" />
<img width="794" height="592" alt="Screenshot 2026-03-27 at 9 41 27 PM" src="https://github.com/user-attachments/assets/1a434b04-edbb-49fc-8c01-3822a534e320" />


## Queries:
<img width="476" height="229" alt="Screenshot 2026-03-31 at 10 31 13 AM" src="https://github.com/user-attachments/assets/9a163f91-1f96-4333-8783-2877474ea5c2" />
<img width="550" height="297" alt="Screenshot 2026-03-31 at 10 29 50 AM" src="https://github.com/user-attachments/assets/c7ba8da8-f36b-43d0-a01c-cadefb504394" />

**Query 1:** Dorms with the highest maintenance activity

**What it does:**
The dorms with the highest number of maintenance requests are displayed by this query. After connecting dorms to rooms, rooms to students, and students to maintenance requests, it calculates the number of requests that originated from each dorm.

<img width="715" height="81" alt="Screenshot 2026-03-31 at 10 32 34 AM" src="https://github.com/user-attachments/assets/6bc64b90-2db2-437a-9397-3fa51b79f94f" />
<img width="716" height="239" alt="Screenshot 2026-03-31 at 10 32 48 AM" src="https://github.com/user-attachments/assets/98182140-13f1-479e-a377-9bc11f865849" />

**Query 2:** Students who have unpaid or pending payments

**What it does:**
This finds students who have not made all of their payments. Students with unpaid, failed, or pending balances might be identified with its help.

<img width="715" height="142" alt="Screenshot 2026-03-31 at 10 34 20 AM" src="https://github.com/user-attachments/assets/716b9be0-0aea-4ae5-8c50-de7b5417e3fc" />
<img width="709" height="390" alt="Screenshot 2026-03-31 at 10 34 49 AM" src="https://github.com/user-attachments/assets/62f73ea8-ed4a-42aa-a11d-0595c9a03363" />

**Query 3:** Average room size by dorm

**What it does:**
This determines each dorm's average room size. It makes it easier to compare which dorms typically have bigger or smaller rooms.


## Database information:
Name of database: al_isj44731. 
Each query listed above has been implemented and stored in the database as a stored procedure.
