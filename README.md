##Project Overview
The purpose of this project is to demonstrate SQL skills by creating a database that tracks users, login activity, devices, and security alerts.

##Project Objectives
Database design
Creating and managing tables
Writing SQL queries
Monitoring login activity
Identifying suspicious login behavior

##Database Tables
Roles
Users
Devices
Login_attempt
security_alert

##SQL Investigations

Failed Login Attempts
Find unsuccessful login attempts:
SELECT *
FROM login_attempts
WHERE login_status = 'FAILED';

Find IP addresses with more than 3 failed attempts:

SELECT
    ip_address,
    COUNT(*) AS failed_attempts
FROM login_attempts
WHERE login_status = 'FAILED'
GROUP BY ip_address
HAVING COUNT(*) >= 3;

##Technologies Used
PostgreSQL
pgAdmin 4
SQL

SQL Skills Demonstrated
CREATE TABLE
INSERT statements
SELECT queries
Filtering with WHERE
JOIN operations
GROUP BY
COUNT functions
Primary keys
Foreign keys
Database relationships
