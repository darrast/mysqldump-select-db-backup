# mysqldump-select-db-backup
A simple interactive bash scritp to create a MySQL database backup selected from all the databases available on the server
for a given MySQL user.

## Prerequisites

MySQL user name and password have been previously stored in the hidden file .my.cnf under $HOME directory. 

```
[client]
user = mysql username
password= "password"
```

```diff
- WARNING
+ User name and password will be stored in **plain text**, so you should know the risks you assume in case 
+ your system gets compromised.
```

## Running the script
When the script is executed displays a **Menu list** with all the databases that the user has permissions to access on the server. MySQL root user is used in this example. Filling the prompt with a number will choose the database we want to be backed up and stored in the directory assigned to **$bak_path** variable. After backup is done it is possible to choose another database as many times as we want or **Exit** the script.
