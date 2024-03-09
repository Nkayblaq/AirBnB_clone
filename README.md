# AirBnB_clone Project Description

This is the first part of the AirBnB clone project where I worked on the backend of the project while interfacing it with a console application with the help of the cmd module in python.

Data (python objects) generated are stored in a json file and can be accessed with the help of the json module in python.

## Description of the command interpreter:
The interface of the application is just like the Bash shell except that this has a limited number of accepted commands that were solely defined for the purposes of the usage of the AirBnB website.

This command line interpreter serves as the frontend of the web app where users can interact with the backend which was developed with python OOP programming.
Some of the commands available are:

+ show
+ create
+ update
+ destroy
+ count

And as part of the implementation of the command line interpreter coupled with the backend and file storage system, the folowing actions can be performed:

+ Creating new objects (ex: a new User or a new Place)
+ Retrieving an object from a file, a database etc…
+ Doing operations on objects (count, compute stats, etc…)
+ Updating attributes of an object
+ Destroying an object

## How to use it
It can work in two different modes:

Interactive and Non-interactive.

In Interactive mode, the console will display a prompt (hbnb) indicating that the user can write and execute a command. After the command is run, the prompt will appear again a wait for a new command. This can go indefinitely as long as the user does not exit the program.
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
In Non-interactive mode, the shell will need to be run with a command input piped into its execution so that the command is run as soon as the Shell starts. In this mode no prompt will appear, and no further input will be expected from the user.
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
## Usage

| Command | Description |
| --- | ---|
| Run the console | ./console.py |
| Quit the console | (hbnb) quit |
| Display the help for a command | (hbnb) help <command> |
| Create an object (prints its id) | (hbnb) create <class> |
| Show an object | (hbnb) show <class> <id> or (hbnb) <class>.show(<id>) |
| Destroy an object | (hbnb) destroy <class> <id> or (hbnb) <class>.destroy(<id>) |
| Show all objects, or all instances of a class | (hbnb) all or (hbnb) all <class> |
| Update an attribute of an object | (hbnb) update <class> <id> <attribute name> "<attribute value>" or (hbnb) <class>.update(<id>, <attribute name>, "<attribute value>") |

## Testing
All the tests should be executed by using this command: 
```bash
python3 -m unittest discover tests
```
You can also test file by file by using this command: 
```bash
python3 -m unittest tests/test_models/test_base_model.py
```


