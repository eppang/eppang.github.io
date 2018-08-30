---
layout: project
type: project
image: images/main.jpg
title: Records Database
permalink: projects/recordsdatabase
# All dates must be YYYY-MM-DD format!
date: 2018-03-11
labels:
  - C
  - Unix
summary: A database with a user interface that allows the user to add, search, or delete a record.
---

<img class="ui medium right floated rounded image" src="../images/database.gif">

## About
The Records Database is a project I did for ICS 212 on UH Unix which contains functions and a user interface that shows the user a menu of choices for a database application. The program starts off as a blank database, and prompts the user with 5 options: Add a new record, print record information, print all database information, delete an existing record, and quit. The options are listed 1-5, and the user can choose one by typing the corresponding number. Each record has an account number, a name, and an address. After records have been added to the database, the database will retain the information of those records even after the program has been closed. Additionally, the program will sort the list by the different account numbers and increment a record if its account number is the same as an existing record.

## Roles and Responsibilities
This project was a homework assignment for ICS 212, and therefore I did not work on a team for this. I was responsible for creating everything, which included the user interface, the driver, the function to write a record into a database, and the function to read a file in a database.

## What I learned
In completing this project, I learned how to program with the user's best interest in mind; this means programming something based on how a user might see things, not how I might see things. I learned how to create something that's useer-friendly and easy to use. This project also taught me the importance of pointers in the C language, and to be careful when assigning values to different variables.
 
Source: <a href="https://github.com/theVacay/vacay"><i class="large github icon"></i>theVacay/vacay</a>
