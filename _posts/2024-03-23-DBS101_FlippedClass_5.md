---
Title: DBS101 Flipped Class 5
categories: [DBS101, Flipped_Class_5]
tags: [DBS101]
---

### Topic: Normalization

From what I have learned, Data normalization is a process used in database design to organize databsase structure efficiently and to reduce data redunancy(repetition). It involves breaking down a database into smaller, logical units and establishing relationships between them and the main aim is to minimize data repetition and dependence therefore, improving data integrity.


#### Types of Normal form
During my cousrse of diving through normalization I found out that there are different types of normal form
    https://miro.medium.com/v2/resize:fit:1400/format:webp/1*2e4BcaGoJB_H9q5MqGmI9Q.png

### First Nomal  form (1NF)
There are basic principle or rule for the database to be in a First normal form: 
    1. The database should have single valued attributes or columns
    2. All the values should be of the same domain.
    3. All the columns in the table should have unique names
    4. The order in which data is stored should not matter 

    https://www.dummies.com/wp-content/uploads/399618.image1.jpg



let me show you a example, in the following table as said in the above rules each column should contain only single value but in this case there are more one values in the subject column.
    https://miro.medium.com/v2/resize:fit:1400/format:webp/1*wMW2xLwFAcfMhhyr3wWemQ.png

So to fix this we just need to break the values in the singl values as shown in the table below.
    https://miro.medium.com/v2/resize:fit:1400/format:webp/1*ngaofQWIozI59t7S-7zEJg.png

---
### Second normal form (2NF)
This form also has some basic principle to be followed for the data to be in 2NF. The principle are;
    1. First and fore most the table should be in 1NF.
    2. There should not be any Partail Dependency.

Before we dive in let me tell you what Partail Dependency is, It an attribute in a table that depends on only a part of the primary key but not the whole key.

for example,
In the table given below we have partial dependency and here is how, 

Emplyoo-Task 
Employee_ID | Task_No | Employee_Name | Task_Name
------------|---------|---------------|-----------------
C01         |  34     |   Mona        | App Development
CO2         | 58      |  Genine       | UX/UI Designing

the non-primary keys are Employee_Name and Task_Name. Employee_Name can be determined by Employee_ID and Task_Name and can be determined by Task_No. Thus the table(Employee-Task) relation would  violate the 2NF in normalization and is considered a bad database design, So we decompose the table to remove the Partail Dependence 

Employee_Info

Employee_ID | Task_No | Employee_Name | 
------------|---------|---------------|
C01         |  34     |   Mona        | 
CO2         | 58      |  Genine       |


Task_Info

 Task_No | Task_Name 
---------|------------
 34      | App Development         
 58      | UX/UI Designing      

Thus, the relation happens to be in the second normal form in the case of Database Normalization.

---

### Third Normal form (3NF)
Same as 1NF and 2NF, 3NF also has some rule to be followed and they are;
    1. the table should be in Second normal form.
    2. And the table should not have Transitive Dependency.

And again before I say anything further let me tell you what Trasitive Dependency is, 
"Transitive Dependency refers to some non-primary key other than the primary key that depends on another non-primary akey that is dependent entirely on the primary key."

Example,
The table below is not in  3NF because it includes a transitive dependency,

Show_ID     | Telecast_ID | Telecast_Type | CD_Cost ($)
------------|---------|---------------|-----------------
F08        |  S09     |   Thriller        | 50
F03         | S05      |  Romantic       | 30

Since, Show_ID is related to Tecast_ID AND Telecast_ID is related to Telecast_Type therfore, there exist a Trasitive Dependency as one non-primary key is related to another non-primary key.

So to solve this we need spilt the table to remove the voilation of 3NF.

Show

Show_ID     | Telecast_ID |   CD_Cost ($)
------------|-------------|-----------------
F08         |  S09         | 50
F03         | S05          | 30

Telecast
 Telecast_ID| Telecast_Type | 
------------|---------------|
S09         |  Thriller
S05         | Romantic

So now  the above table is now on 3NF of normalization.

---

### Boyce-codd normal form (BCNF)
Its is a extention of third noraml form and is also known as 3.5 normal form. and like any other normal form it also has some conditions to be followed;
    1. The table shoul be Third noraml form 
    2. And, for a dependency A-->B, A, can not be non-primary attribute, if B, is a primary attritube.

If a non-primary attribute determines a primary attritube than it does not satisfy the BCNF. Inorder to do it we need to decompose table.

Below in the table is an example how we can table into BCNF:

Student_ID  | Subject     |   Professor
------------|-------------|-----------------
101         | Java        | P.Java
101         | C++         | P.Cpp
102         | Java        | P.Java2
103         | C#          | P.Chash

In the table above the primary key are Student_ID + Subject, because using these two we can find all the  columns in the table. One professor teaches only one subject, but one subject may have two different professors. So we see there is dependency there where the subject is depending on the professor name. And since the subject being the primary attribute, and professor being the non-primary attribute which is not allowed in BCNF.

To fix this we decompose the table into two tables "Student" and "Professor" table,

Student

Student_ID  | p_ID     |  
------------|-------------|
101         | 1        | 
101         | 2         | 
102         | 3        | 
103         | 4         | 

Professor
P_ID  | Subject     |   Professor
------|-------------|-----------------
1     | Java        | P.Java
2     | C++         | P.Cpp
3     | Java        | P.Java2
4     | C#          | P.Chash

Now the table will satify BCNF.

---

### Fourth normal form (4NF)

For a table to satisfy 4NF the following condition should be full filled;
    1. The table should be in BCNF
    2. The table should not have Multi-valued Dependency.

Example;
The table below shows the college enrolment table with columns s_id, course and hobby.

    - s_ID being the primary key 
    - course is multi-valued attribute
    - hobby is the attribute that does not depend on the course.

s_ID   |   course   |  hobby
-------|------------|--------
1      |  science   | football
1      | math       |  vollyball
2      |   EVS      |  cricket
2      |  history   |  baseball

Now to make the table into 4NF we need to decompose the table into two.

R1(student-couser) table
s_ID   |   course   
-------|------------
1      |  science   
1      | math       
2      |   EVS      
2      |  history   

R2(student-hobby) table

s_ID   |   hobby   
-------|------------
1      |  fotball   
1      | vollyball       
2      |   cricket      
2      |  baseball

Now the tables are in 4NF, there are no multi-valued dependencies, and all functionally dependind on the primary key.

