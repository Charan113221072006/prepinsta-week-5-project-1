# SQL Murder Mystery Solver

## Overview

This Python script uses SQLite to interact with a database related to a murder mystery investigation. The investigation involves querying various tables to gather information, analyze witness statements, identify suspects, and solve the mystery. The script includes SQL queries for extracting relevant data and updates the solution with the discovered information.

## Database Connection

The script connects to an SQLite database named 'crime_scene.db' using the `sqlite3` library.

```python
import sqlite3 as sql

# Connect to the database
conn = sql.connect('crime_scene.db')
cursor = conn.cursor()
```

## Queries and Analysis

### Crime Scene Report

The initial query retrieves the crime scene report for a specific date and city.

### Witness Statements

Queries are performed to identify key witnesses based on their locations and names. The information is used to extract interview transcripts.

### Suspect Identification

The script identifies suspects based on gym check-ins, membership status, and specific observations. The suspects' details are then inserted into the 'solution' table.

### Solution and Further Investigation

The script updates the solution with the identified suspect's name and retrieves further information from an interview transcript.

### Advanced Analysis

Advanced queries are performed to narrow down potential suspects based on specific criteria, such as gender, hair color, car details, income, and attendance at a concert. The final suspect is identified and added to the solution.

## Solution Verification

The script verifies and retrieves the final solution value from the 'solution' table.

## Usage

1. Ensure the `sqlite3` library is installed.
2. Download the SQLite database file ('crime_scene.db') containing the necessary tables.
3. Update the script with the correct database file path.
4. Run the script to perform the SQL queries, identify suspects, and solve the murder mystery.

Feel free to customize the script for different murder mystery scenarios or database structures.

---

