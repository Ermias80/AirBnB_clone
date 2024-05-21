AirBnB clone
=======

Description
======

This team project primarily focuses on enhancing the console component of an Airbnb clone. This repository houses the initial phase of a student project dedicated to developing a clone of the Airbnb website. In this phase, we have implemented a backend interface, or console, designed to manage the application's data. The console commands enable users to create, update, and delete objects, as well as manage file storage.


Command Interpreter
=======
Command interpreter is a shell like with limited to a specific use-case. It can be used to test the functionality of the supported storage engines as well. You can find some examples of its usage[ here](#examples). In this project the Command interpreter will help to manage the objects of our project, Like:

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

 ```bash
git clone git@github.com:Mahari9/AirBnB_clone_v2.git
cd AirBnB_clone_v2
```
- Run the console.py file with: "./console.py" or "python console.py"
- When this command is run the following prompt should appear:
```
(hbnb)
```
- This prompt designates you are in the "HBnB" console. There are a variety of commands available within the console program.
- And finally type "help" in the console for documentation.
Interactive Mode
```bash
$ ./console.py
(hbnb) help
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
(hbnb)
(hbnb) quit
$
```
Non-Interactive Mode
```bash
$ echo "help" | ./console.py
(hbnb)
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```
##### Commands
    * create - Creates an instance based on given class
    * destroy - Destroys an object based on class and UUID
    * show - Shows an object based on class and UUID
    * all - Shows all objects the program has access to, or all objects of a given class
    * update - Updates existing attributes an object based on class name and UUID
    * quit - Exits the program (EOF will as well)




### Available Models
These are the models that are currently available.
| Class | Description |
|:-|:-|
| BaseModel | A(n abstract) class that represents the base class for all models (all models are instances of this class). |
| User | Represents a user account. |
| State | Represents the geographical state in which a _User_ lives or a _City_ belongs to. |
| City | Represents an urban area in a _State_. |
| Amenity | Represents a useful feature of a _Place_. |
| Place | Represents a building containing rooms that can be rented by a _User_. |
| Review | Represents a review of a _Place_. |




### Alternative Syntax
* Users are able to issue a number of console command using an alternative syntax:
	Usage: <class_name>.<command>([<id>[name_arg value_arg]|[kwargs]])
+ Advanced syntax is implemented for the following commands: 
    * all - Shows all objects the program has access to, or all objects of a given class
	* count - Return number of object instances by class
    * show - Shows an object based on class and UUID
	* destroy - Destroys an object based on class and UUID
    * update - Updates existing attributes an object based on class name and UUID

##### Examples
###  Testing
+ Within the project, we have incorporated unit tests to verify the accuracy of the implemented functionality. To execute these tests, follow the instructions below:
+ - "python3 -m unittest discover tests" (interactive mode)
+ - "echo 'python3 -m unittest discover tests' | bash" (Non-interactive mode)

