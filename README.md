AirBnB clone
=======

Description
======

This team project primarily focuses on enhancing the console component of an Airbnb clone. This repository houses the initial phase of a student project dedicated to developing a clone of the Airbnb website. In this phase, we have implemented a backend interface, or console, designed to manage the application's data. The console commands enable users to create, update, and delete objects, as well as manage file storage.


Command Interpreter
=======
Command interpreter is a shell like with limited to a specific use-case. It can be used to test the functionality of the supported storage engines as well. You can find some examples of its usage here. In this project the Command interpreter will help to manage the objects of our project, Like:

+ To update/create a new object
+ To retrive an object from a file, database, etc..
+ To update attributes of an object
+ To do operations on objects (count, compute stats, etc…)
+ To destroy an object

## Environment
+ Language: Python3
+ OS: Ubuntu 20.04 LTS

## Environment Variables
+ HBNB_ENV: The running environment. It can be dev or test.
+ HBNB_MYSQL_USER: The MySQL server username.
+ HBNB_MYSQL_PWD: The MySQL server password.
+ HBNB_MYSQL_HOST: The MySQL server hostname.
+ HBNB_MYSQL_DB: The MySQL server database name.
+ HBNB_TYPE_STORAGE: The type of storage used. It can be file (using FileStorage) or db (using DBStorage).

# General Use
To start the command interpreter, follow these steps:
+ Clone the project repository to your local machine and Navigate to the directory that contain the file.


<br>
<br>
<center> <h2>Examples</h2> </center>
## Testing
Within the project, we have incorporated unit tests to verify the accuracy of the implemented functionality. To execute these tests, follow the instructions below:
- "python3 -m unittest discover tests" (interactive mode)
- "echo 'python3 -m unittest discover tests' | bash" (Non-interactive mode)

### Examples

<h3>Primary Command Syntax</h3>

###### Example 0: Create an object
@@ -133,31 +137,31 @@ Usage: create <class_name>
```
(hbnb) create BaseModel
3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb)                   
(hbnb)
```

###### Example 1: Show an object
Usage: show <class_name> <_id>

```
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc-efb6-4041-bfe9-3cc9727588f8', 'created_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96959), 
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc-efb6-4041-bfe9-3cc9727588f8', 'created_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96959),
'updated_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96971)}
(hbnb)  
(hbnb)
```
###### Example 2: Destroy an object
Usage: destroy <class_name> <_id>
```
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
** no instance found **
(hbnb)   
(hbnb)
```
###### Example 3: Update an object
Usage: update <class_name> <_id>
```
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) show BaseModel b405fc64-9724-498f-b405-e4071c3d857f
[BaseModel] (b405fc64-9724-498f-b405-e4071c3d857f) {'id': 'b405fc64-9724-498f-b405-e4071c3d857f', 'created_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729889), 
[BaseModel] (b405fc64-9724-498f-b405-e4071c3d857f) {'id': 'b405fc64-9724-498f-b405-e4071c3d857f', 'created_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729889),
'updated_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729907), 'first_name': 'person'}
(hbnb)
```
@@ -195,8 +199,3 @@ Usage: <class_name>.update(<_id>, <dictionary>)
(hbnb) ["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'name': 'Fred the Frog', 'age': 9, 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```
<br>
## Testing
Within the project, we have incorporated unit tests to verify the accuracy of the implemented functionality. To execute these tests, follow the instructions below:
- "python3 -m unittest discover tests" (interactive mode)
- "echo 'python3 -m unittest discover tests' | bash" (Non-interactive mode)
