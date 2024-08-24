# A-Level Coursework

This repository contains the code and documentation for my A-Level coursework project.

## Description

My project was creating a dentist database management system allowing for booking of appointments and managing patient information. The system is stored in a relational database using SQLite and utilizes Tkinter for the GUI.

# Features

- **File Encryption**:
  - Encrypts a file using the Fernet encryption method.
  - Deletes the original file after encryption.

- **File Decryption**:
  - Decrypts a file using the Fernet decryption method.
  - Deletes the encrypted file after decryption.

- **Quit and Logout**:
  - Prompts the user for confirmation to quit or logout.
  - Encrypts the database file.
  - Destroys the current window.
  - Logs the logout time and StaffID if provided.
  - Reopens the login window if the choice is "Logout".

- **Validation Routines**:
  - **Presence Check**: Ensures a field is not empty.
  - **Range Check**: Ensures a field's value is within a specified range.
  - **Length Check**: Ensures a field's length is within specified bounds.
  - **Type Check**: Ensures a field's value is of a specified type.
  - **Format Check**: Ensures a field's value matches a specified format.

- **Database Backup**:
  - Periodically or manually backs up the database.
  - Logs the backup date.
  - Copies the database file to a backup directory.

- **Logging**:
  - Logs the time and date when a user logs into the system.

- **Login**:
  - Handles user login.
  - Decrypts the database file.
  - Validates the entered StaffID and Password against the database.
  - Logs the login time and StaffID.
  - Opens the main application screen if login is successful.
  - Encrypts the database file again after validation.

- **Access Control**:
  - Determines if a user has access to a specific table based on their access level.

- **Dropdown Menu Creation**:
  - Creates a dropdown menu for selecting fields from a table.
  - Adjusts the options based on the table and access level.

- **Calendar Widget**:
  - Creates a calendar widget pre-selected with today's date.
  - Allows the user to select a date.

- **Payslip Creation and Sending Payslip**:
  - Generates and sends payslips to all staff members.
  - Ensures the database is not operational while emails are being sent.

- **Reminder Email Sending**:
  - Sends a reminder email to a patient about their appointment.
  - Requires the patient ID to find the email address.

- **Report Creation and Saving Report**:
  - Generates a report including staff pay and a graph of profit for the past month.
  - Saves the report as a `.docx` file.

- **Graph Creation and Saving**:
  - Creates a bar graph of profits over the past month and saves it as 'figure1.png'.

- **Database Query Execution**:
  - Executes a given SQL query with provided data on the database.

- **Record Retrieval**:
  - Retrieves the selected record from a treeview and returns it as a 2D array.

- **Treeview Refresh**:
  - Refreshes the treeview to reflect changes made to the database.

- **Record Deletion**:
  - Deletes a selected record from the database if the user has the appropriate access level.

- **Record Search**:
  - Searches for a record in the database based on a search term and updates the treeview with the results.

## Usage

To use this project, navigate to the project directory and run the main Python file:

```
cd A-Level-Coursework
python main.py
```

## Access Levels 

EVERYONE CAN QUIT, LOGOUT AND BACKUP THE SYSTEM 

access level 0 (management)- do everything everywhere
StaffID: 1 Password: password

access level 1 (accounting staff) - do everything everywhere apart from patient table
StaffID: 2 Password: password

access level 2 (dentist) - do everything on appointment, AppointmentTreatment, AppointmentMaterial and Treatment 
VIEW ONLY staff and AppointmentStaff table (only view their record)
StaffID: 3 Password: password 

access level 3 (receptionist) - do everthing on appointment and patient only
VIEW ONLY staff (only view their record)
StaffID: 4 Password: password  

access level 4 (dental assistent and cleaning staff) - VIEW ONLY staff and AppointmentStaff table (only view their record)
StaffID: 5 Password: password 