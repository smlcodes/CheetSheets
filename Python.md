Intro
------------------------
Python can be used on a server to create web applications.
Python can be used alongside software to create workflows.
Python can connect to database systems. It can also read and modify files.
Python can be used to handle big data and perform complex mathematics.
Python can be used for rapid prototyping, or for production-ready software development.


python --version

Running python from File
python helloworld.py


Running Python from Interactive CmdLine
C:\Users\Your Name>python
Python 3.6.4 (v3.6.4:d48eceb, Dec 19 2017, 06:04:45) [MSC v.1900 32 bit (Intel)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello, World!")


exit() 		//closing shell


Python Syntax
------------------------------------------
Python uses indentation to indicate a block of code. ( {} in other programming lang's)

#This is a comment		//single line

"""				//Multi line
This is a comment
written in
more than just one line
"""


Variabless
----------------------
x = 5		//Integer variable
y = "John"	//String variable

x = 4 # x is of type int
x = "Sally" # x is now of type str


#######################################################################
				Data Types
#######################################################################
Text Type	:	str
Numeric Types	:	int, float, complex
Collection Types:	list, tuple, range
Mapping Type	:	dict
Set Types	:	set, frozenset
Boolean Type	:	bool
Binary Types	:	bytes, bytearray, memoryview
type()		:	get the data type of any object.

----------------------------------------------------------------------s
Example						Data Type
----------------------------------------------------------------------
x = "Hello World"				str	
x = 20						int	
x = 20.5					float	
x = 1j						complex	
x = ["apple", "banana", "cherry"]		list	
x = ("apple", "banana", "cherry")		tuple	
x = range(6)					range	
x = {"name" : "John", "age" : 36}		dict	
x = {"apple", "banana", "cherry"}		set	
x = frozenset({"apple", "banana", "cherry"})	frozenset	
x = True					bool	
x = b"Hello"					bytes	
x = bytearray(5)				bytearray	
x = memoryview(bytes(5))			memoryview	

Number Datatypes
-----------------
x = 1    # int
y = 2.8  # float
z = 1j   # complex	//Complex numbers are written with a "j" as the imaginary part.
			## You cannot convert complex numbers into another number type.

Strings
-----------------
#Single line Strings
a = "Hello"


#Multi line Strings

//three double quotes
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""

//Or three single quotes
a = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''


# Strings are Arrays.
strings in Python are arrays of bytes.Python does not have a character data type, a single character is simply a string with a length of 1.

a = "Hello, World!"
print(a[0])
print(a[1])
print(a[2])

C:\Users\Satya>a.py
H
e
l

## Get the characters from position 2 to position 5 (not included):
b = "Hello, World!"
print(b[2:5])
o/p:llo

## len() returns the length of a string:
a = "Hello, World!"
print(len(a)) //13

## strip() removes whitespace from the beginning or the end:
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"



## lower() returns string in lower case, upper() returns the string in upper case:
a = "Hello, World!"
print(a.lower())
print(a.upper())


## More String methods
print(a.split(",")) # returns ['Hello', ' World!']




Boolean
----------------------------
Booleans represent one of two values: "True" or "False"



###############################################################################
		Python Collections (Arrays)
###############################################################################
There are four collection data types in the Python programming language:
List 		-elements are ordered and changeable. Allows duplicate members.
Tuple		-elements are ordered and unchangeable. Allows duplicate members.
Set		-elements are unordered and unindexed. No duplicate members.
Dictionary	-elements are unordered, changeable and indexed. No duplicate members.


List
------------------
list = ["apple", "banana", "cherry"]

print(thislist[0]) //apple
print(thislist[1]) //banana

print(len(thislist))//3

thislist.append("orange") //['apple', 'banana', 'cherry', 'orange']

thislist.insert(1, "orange")

thislist.remove("banana")

The "del" keyword removes the specified index / complete list
del thislist[0]
del thislist


Make a copy of a list with the copy() method:
mylist = thislist.copy()


Note: Python does not have built-in support for Arrays, but Python Lists can be used instead.


Tuple
----------------------------------
A tuple is a collection which is ordered and unchangeable. In Python tuples are written with round brackets.

thistuple = ("apple", "banana", "cherry")
print(thistuple)



You cannot add items to a tuple:
thistuple = ("apple", "banana", "cherry")
thistuple[3] = "orange" # This will raise an error
print(thistuple)
# TypeError: 'tuple' object does not support item assignment

Remaining functions same as List



Set
------------------------------
A set is a collection which is unordered and unindexed. In Python sets are written with curly brackets.

thisset = {"apple", "banana", "cherry"}
print(thisset)


thisset.add("orange")

thisset.remove("banana")




Dictionary
---------------------------------------
A dictionary is a collection which is unordered, changeable and indexed.
In Python dictionaries are written with curly brackets, and they have keys and values.


thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)


## You can access the items of a dictionary by referring to its key name, inside square brackets:
x = thisdict["model"]
print(x) //Mustang

or

x = thisdict.get("model")
print(x) //Mustang







########################################################
		Conditional Statements
########################################################


if
--------------------
 "if statement" is written by using the 'if' keyword & ends with ':'

syntax :
if <condition> :


a = 33
b = 200
if b > a:
  print("b is greater than a")

Indentation
Python relies on indentation (whitespace at the beginning of a line) to define scope in the code. Other programming languages often use curly-brackets for this purpose.

a = 33
b = 200
if b > a:
print("This will Throws ERROR ")
#IndentationError: expected an indented block


if...else
------------------------
a = 200
b = 33
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")


if...elif....else
-----------------------
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")



NOTE:
if statements cannot be empty, but if you for some reason have an if statement with no content, put in the pass statement to avoid getting an error.

Example
a = 33
b = 200

if b > a:
  pass


##########################################################################
				LOOPS
##########################################################################


While loop
---------------------------
Print i as long as i is less than 6:

i = 1
while i < 6:
  print(i)
  i += 1


while...else
Print a message once the condition is false:

i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")


for loop
-----------------
A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

## Print each fruit in a fruit list:
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)

## Loop through the letters in the word "banana":
for x in "banana":
  print(x)


## Print all numbers from 0 to 5, and print a message when the loop has ended:
for x in range(6):
  print(x)
else:
  print("Finally finished!")





#####################################################################
			Python Functions
#####################################################################

A function is a block of code which only runs when it is called.
You can pass parameters into a function.
A function can return data as a result.

In Python a function is defined using the "def" keyword:
def my_function():
  print("Hello from a function")

To call a function, use the function name followed by parenthesis.
my_function()


## with args
def my_function(fname):
  print(fname + " Kaveti")

my_function("Satya")
my_function("Mounika")
my_function("Sravani")


## If the number of arguments is unknown, add a * before the parameter name:
def my_function(*kids):
  print("The youngest child is " + kids[2])
my_function("Emil", "Tobias", "Linus")


## Return Values
To let a function return a value, use the return statement:

def my_function(x):
  return 5 * x
print(my_function(3))
print(my_function(5))
print(my_function(9))


## function definitions cannot be empty, but if you for some reason have a function definition with no content, put in the pass statement to avoid getting an error.
def myfunction():
  pass




###################################################
		LAMBDA
###################################################
A lambda function is a small anonymous function.
A lambda function can take any number of arguments, but can only have one expression.

Syntax
lambda arguments : expression


A lambda function that adds 10 to the number passed in as an argument, and print the result:
x = lambda a : a + 10
print(x(5))


A lambda function that multiplies argument a with argument b and print the result:
x = lambda a, b : a * b
print(x(5, 6))




####################################################################################
				Python Classes
####################################################################################

Create a class named MyClass, with a property named x:
class MyClass:
  x = 5

Create an object named p1, and print the value of x:
p1 = MyClass()
print(p1.x)


All classes have a function called __init__(), which is always executed when the class is being initiated.(kind of Constrcutor in java).s
Use the __init__() function to assign values to object properties, or other operations that are necessary to do when the object is being created:

"self" parameter is a reference to the current instance of the class.(this in Java)

class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()



Self does not have to be named self , you can call it whatever you like, but it has to be the first parameter of any function in the class:

class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()



################################################################
			Python Inheritance
################################################################

## Create a class named Person, with firstname and lastname properties, and a printname method:
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:
x = Person("John", "Doe")
x.printname()


## Create a class named Student, which will inherit the properties and methods from the Person class:
class Student(Person):
  pass
Note: Use the pass keyword when you do not want to add any other properties or methods to the class.

Use the Student class to create an object, and then execute the printname method:
x = Student("Mike", "Olsen")
x.printname()



# If you need to create a global variable, but are stuck in the local scope, you can use the global keyword.
The global keyword makes the variable global.
def myfunc():
  global x
  x = 300

myfunc()

print(x)







##########################################################################
			Python Exception Handling
##########################################################################

-try block lets you test a block of code for errors.
-except block lets you handle the error.
-finally block lets you execute code, regardless of the result of the try- and except blocks.


# If we execute below one, excception will Occure& wont proceed furthur
print(x)
print("After Exception...")
------------o/p------------------------
    print(x)
NameError: name 'x' is not defined



# The try block will generate an exception, because x is not defined:
try:
  print(x)
except:
  print("An exception occurred")

print("After Exception...")

-----------op------------
An exception occurred
After Exception...



# Print one message if the try block raises a NameError and another for other errors:
try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")




# The finally block, if specified, will be executed regardless if the try block raises an error or not.
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")


# Raise an error and stop the program if x is lower than 0:
x = -1
if x < 0:
  raise Exception("Sorry, no numbers below zero")




##########################################
	File Handling
##########################################

The open() function takes two parameters; filename, and mode.There are four different methods (modes) for opening a file:
"r" - Read - Default value. Opens a file for reading, error if the file does not exist
"a" - Append - Opens a file for appending, creates the file if it does not exist
"w" - Write - Opens a file for writing, creates the file if it does not exist
"x" - Create - Creates the specified file, returns an error if the file exists

In addition you can specify if the file should be handled as binary or text mode
"t" - Text - Default value. Text mode
"b" - Binary - Binary mode (e.g. images)

To open a file for reading it is enough to specify the name of the file:
f = open("demofile.txt")

The code above is the same as:
f = open("demofile.txt", "rt")

Because "r" for read, and "t" for text are the default values, you do not need to specify them.
Note: Make sure the file exists, or else you will get an error.


Reading:
The open() function returns a file object, which has a read() method for reading the content of the file:
f = open("demofile.txt", "r")
print(f.read())

## Return the 5 first characters of the file:
f = open("demofile.txt", "r")
print(f.read(5))


## You can return one line by using the readline() method.Read one line of the file:
f = open("demofile.txt", "r")
print(f.readline())


## By calling readline() two times, you can read the two first lines:
f = open("demofile.txt", "r")
print(f.readline())
print(f.readline())


## By looping through the lines of the file, you can read the whole file, line by line:
f = open("demofile.txt", "r")
for x in f:
  print(x



Write to an Existing File
To write to an existing file, you must add a parameter to the open() function:
"x" - Create - will create a file, returns an error if the file exist
"a" - Append - will append to the end of the file
"w" - Write - will overwrite any existing content

f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()


Delete a File
To delete a file, you must import the OS module, and run its os.remove() function:
import os
os.remove("demofile.txt"

## Check if file exists, then delete it:
import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist")


## Remove the folder "myfolder":

import os
os.rmdir("myfolder")
Note: You can only remove empty folders.




##########################################################################
			Python PIP
##########################################################################
PIP is a package manager for Python packages, or modules.(like MAVEN in java)





##########################################################################
				Python MySQL
##########################################################################

Python needs a MySQL driver to access the MySQL database.

PIP to install "MySQL Connector".
python -m pip install mysql-connector


There are the following steps to connect a python application to our database.
- import mysql.connector module
- Create the connection object.
- Create the cursor object
- Execute the query



## Test Connection
import mysql.connector

#Create the connection object  
mydb = mysql.connector.connect(
  host="localhost",
  user="root",
  passwd=""
)

#printing the connection object
print(mydb)
//<mysql.connector.connection.MySQLConnection object at 0x00898130>



## create a database named "mydatabase":

import mysql.connector
mydb = mysql.connector.connect(
  host="localhost",
  user="root",
  passwd=""
)
mycursor = mydb.cursor()
mycursor.execute("CREATE DATABASE mydatabase")

cursor() - is like create Statememnt Object in Java


## Return a list databases
mycursor.execute("SHOW DATABASES")
for x in mycursor:
  print(x)


## Create Table with primary:

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="root",
  passwd="",
  database="mydatabase"
)

mycursor = mydb.cursor()
mycursor.execute("CREATE TABLE customers (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), address VARCHAR(255))")


---------------- Examples -----------------------------------

## Create Table with primary:

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="root",
  passwd="",
  database="mydatabase"
)

mycursor = mydb.cursor()

## create Table
mycursor.execute("CREATE TABLE customers (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), address VARCHAR(255))")



## Insert values 
sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"

val = ("John", "Highway 21")
mycursor.execute(sql, val)

mydb.commit()
print(mycursor.rowcount, "record inserted.")



### Insert Multiple Rows
val = [
  ('Peter', 'Lowstreet 4'),
  ('Amy', 'Apple st 652'),
  ('Hannah', 'Mountain 21'),
  ('Michael', 'Valley 345'),
  ('Sandy', 'Ocean blvd 2'),
  ('Betty', 'Green Grass 1'),
  ('Richard', 'Sky st 331'),
  ('Susan', 'One way 98'),
  ('Vicky', 'Yellow Garden 2'),
  ('Ben', 'Park Lane 38'),
  ('William', 'Central st 954'),
  ('Chuck', 'Main Road 989'),
  ('Viola', 'Sideway 1633')
]

mycursor.executemany(sql, val)
mydb.commit()
print(mycursor.rowcount, "was inserted.")
