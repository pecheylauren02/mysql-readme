# Assignment 1: Part 3 of 3 documentation

## MySQL Database Queries for COMPANY1

This repository contains SQL scripts and queries for managing and interacting with the "COMPANY1" database. The dataset includes tables related to employees and departments within the company.

### Project Overview

The **COMPANY1** database consists of two main tables:

- **EMP**: Contains employee information such as employee number, name, job, salary, and commission.
- **DEPT**: Contains department details, including department number, name, and location.

The queries provided in this repository are designed to retrieve and manipulate data for various use cases, such as employee salary analysis, department statistics, and more.

### Table Structures

#### EMP Table

| Column   | Description                                                   |
|----------|---------------------------------------------------------------|
| EMPNO    | Employee number (Primary Key)                                  |
| ENAME    | Employee name                                                 |
| JOB      | Job title of the employee                                      |
| MGR      | Manager's employee number (foreign key to EMPNO)               |
| HIREDATE | Hire date of the employee                                      |
| SAL      | Salary of the employee                                         |
| COMM     | Commission received by the employee (if applicable)            |
| DEPTNO   | Department number (foreign key to DEPT)                        |

#### DEPT Table

| Column   | Description                                                   |
|----------|---------------------------------------------------------------|
| DEPTNO   | Department number (Primary Key)                                |
| DNAME    | Department name                                               |
| LOC      | Location of the department                                     |

## Setup Instructions

1. Clone the repository to your local machine:
- git clone https://github.com/yourusername/company1-database.git

2. Create the Database
Create and use the COMPANY1 database in MySQL:
- CREATE DATABASE COMPANY1;
- USE DATABASE COMPANY1;

3. Create the Tables
- Run the script to create the EMP and DEPT tables in the database

4. Insert Sample Data

## Queries
Below are the SQL queries that retrieve specific information from the database:

1. List all Employees whose salary is greater than 1,000 but not 2,000

- SELECT ENAME, DNAME, SAL
- FROM EMP E
- JOIN DEPT D ON E.DEPTNO = D.DEPTNO
- WHERE SAL > 1000 AND SAL < 2000;

2. Count the number of people in department 30 who receive both a salary and a commission:

- SELECT COUNT(*)
- FROM EMP
- WHERE DEPTNO = 30 AND SAL IS NOT NULL AND COMM IS NOT NULL;



