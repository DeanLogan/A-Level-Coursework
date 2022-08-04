## libraries you must install before operation ##

pip install pillow
pip install python-docx
pip install matplotlib
pip install tk calendar
pip install cryptographys

## validation notes ##

The entire staff table is validated as proof that the validation rountines work. 

The AppointmentMaterial, AppointmentTreatment and Accountancy table are validated so that 
calculations can take place.

You can only add to the accountancy table exactly once a week from the date within the last record. 
It is based on the assumption that it is someone's job to enter this record once a week. This is not an 
error it is the design of the system. It is to ensure that the graph within the report is accurate. If you try
to add to this table not on the correct date then you will be greated with a message box saying you
cannot add to this table. 

## access levels ##

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

## general notes ##

PLEASE MAKE SURE YOU DO NOT HAVE THE DATABASE OPEN IN DB BROWSER WHEN YOU ARE USING THE DATABASE WITH MY CODE.
I HAVE NOT CODED FOR THE DATABASE LOCKED ERROR THAT THIS CAUSES. THE SYSTEM OPERATES UNDER THE 
ASSUMPTION THAT THE USER DOES NOT HAVE ACCESS TO ANY OTHER WAY TO VIEW DATABASES.

There is a folder called databaseSaves which contains a encrypted and decrypted copy of the database if you ever 
find yourself needing them for testing or any other reason.

If there is an error while trying to send the reminder email you might have to change the security settings 
for the smtplib66@gmail.com email as for some reason after a while the less secure apps accsess turns itself 
off. The login for the email is as follows; email:smtplib66@gmail.com, password:yesemail. 
The following is a link on how to change the settings: https://hotter.io/docs/email-accounts/secure-app-gmail/

If you want to check to see the backup is working periodically you can change the date within the backupMadeLog.txt
file to a month ago then check if there is a backup made. I have not encountered any errors while manually changing 
the date. 

While entering in any email please use the smtplib66@gmail.com email as if you use another email it may go to that 
emails spam folder. If you use this email it ensures that you can see that the email has been sent

Please use the Quit button when exiting the system as this is the intended way. This is because if Quit any other 
way the logs of the system will not be taken. It will also cause problems with encryption as the file will be 
decrypted when the user logs in and will be encrypted when the user quits or logs out.
