AirBnB Description:

AirBnB Clone is a dynamic web application, a front-end interface of a clone of AirBnB that integrate a database storage system with a back-end API.

Presently the project only implements the back-end console.

Classes:

AirBnB Clone uses the following classes

First Step is writing a command interpreter to manage the AirBnB objects:
This is the first step towards building a first full web application: the AirBnB clone. This first step is very important because it uses what is built during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help to:

1. put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances
2. create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
3. create all classes used for AirBnB (User, State, City, Place…) that inherit from BaseModel
4. create the first abstracted storage engine of the project: File storage.
5. create all unittests to validate all our classes and storage engine

The Command interpreter (the console) is a Shell with a limited functionality, limited to specific use cases. In this case it will be able to manage the objects of the project:
1. Create a new object (ex: a new User or a new Place)
2. Retrieve an object from a file, a database etc…
3. Do operations on objects (count, compute stats, etc…)
4. Update attributes of an object
5. Destroy an object

The AirBnB clone console can be run both interactively and non-interactively. To run the console in non-interactive mode, pipe any command(s) into an execution of the file console.py at the command line.

To bring out documented commands
$ echo "help" | ./console.py


To use the AirBnB console in inetractive mode, run
$ ./console.py

While riunning in interactive mode the console displays a promt for input:
$ ./console.py
(abnb)

To quit the console enter the command quit or input an EOF signal (ctrl-D)
$ ./console.py
(abnb) quit
$

$ ./console.py
(abnb) EOF
$

Console Commands:
The AirBnB console supports the following commands:

Create
        Usage: create <class>
Creates a new instance of a given class. The class ID is printed and instance is saved to the file.json.

Save
        Usage: show <class> <id> or <class>.show(<id>)
Prints the string representation of a class instance based on a given id.

Destroy
        Usauge: destroy <class> <id> or <class>.destroy(<id>)
        Deletes a class instance based on the given id. The storage file file.json is updated accordingly.

all
        Usage: all or all <class> or <class>.all()
        Prints the string representation of all instances of a given class. If no class name is provided, the command prints all instances of every class.

count
        Usage: count <class> or <class>.count()
        Retrieves the number of instances of a given class.

update
        Usage: update <class> <id> <attribute name> "<attribute value>" or <class>.update(<id>, <attribute name>, <attribute value>) or <class>.update( <id>, <attribute dictionary>).
        Updates a class instance based on a given id with a given key/value attribute pair or dictionary of attribute pairs. If update is called with a single key/value attribute pair, only "simple" attributes can be updated (ie. not id, created_at, and updated_at). However, any attribute can be updated by providing a dictionary.


Testing:

Unittests for the AirBnB project are defined in the tests folder. To run the entire test suite simultaneously, execute the following command:
$ python3 unittest -m discover tests

Alternatively, you can specify a single test file to run at a time:
$ python3 unittest -m tests/test_console.py

