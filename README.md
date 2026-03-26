# MIS4610-Project
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

## Data Dictionary:

## Queries:

## Database information:
