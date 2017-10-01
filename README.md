# Python 3

### About Python

Python 3.0 also known as Python 3000 is an easy to learn, powerful programming language. It has efficient high-level data structures and a simple but effective approach to object-oriented programming. Python’s elegant syntax and dynamic typing, together with its interpreted nature, make it an ideal language for scripting and rapid application development in many areas on most platforms.

### Installing Python 3

##### The first program
Let's write our first program to, print “Hello World !”

In python we use print(“”) function to display text on the screen.
We use quotations marks for beginning and end of the string, they don't appear in the result.
```python
print(“Hello World !”)
```
In two ways we can run python program
- Python Shell
- Python Script

### Using Python Shell

After installing Python on your machine, to open the python shell type in “python3” in your command prompt or terminal, this will begin an interactive python session.This interactive session doesn't save any of your code in a file, it expires as soon as you exit from the shell.

In your python shell, you will find the current running version of your python,some information and three arrows waiting for your command. Now lets write the code to print Hello World in the Python shell.
```python
>>>print(“Hello World !”)
Hello World !
>>>
```
As soon as you hit enter the python interpreter runs the code and gives the output.

General python shell is used to test programs on the go, help(anything) for documentation. It's way faster than any web interface.

### Executing Python Script

To run python scripts save your python code in .py file and in your command prompt or terminal use python3 file_name.py to execute the program.

##### Example:
hello_world.py
```python
print(“Hello World !”)
```
```
$python3 hello_world.py
Hello World !
```
Make sure you change the directory where you saved the file before doing it. When you are writing large pieces of Python code then we need to use Script Mode. You can use different text editors for writing python scripts such as Sublime Text ,Atom Editor.

### Number and Variables
As we know numbers are everywhere, so let’s see how Python deals with numbers.

Python shell can be used as a calculator, you can perform basic mathematical operation in python shell such as addition, division etc.

##### Example:

```
>>>3 + 3
6
>>>(84949*292)/322
77034
>>>
```
In python we have three distinct number types they are integers, floating point numbers, and complex numbers. Integers are numbers with no fractional part they can be either positive or negative or unsigned(zero).Float values are numbers with fractional part.

In programming, a variable is nothing more than a name for something.Variable names are case sensitive.

To declare a variable in Python you have to give its name followed by an equal sign and the initialization value.
```python
var_name = value
myname = “Stark”
pi = 3.14 
```
When you keep assigning the values to the same variable name Python simply replaces the older value with newer value.

Python3 supports the following data types:
Boolean
Integer
Float
Complex
String



```
fuel = True
speed = 167
miles = 153.5
location = 16.789 + 12323.45j
car = "Mustang"

# type() function returns the datatype of variable.

print(fuel, type(fuel))
print(speed, type(speed))
print(miles, type(miles))
print(location, type(location))
print(car, type(car))
```




Note : Never start a variable name with digit.


Data Structures 
To organize and process data in memory efficiently we use data structures, In Python we have different types data structures and several operations to perform on them.

Now we will discuss about three main data structures in Python
Lists 
Lists are ordered,mutable sequence of values,these are similar to arrays in C and C++.

To declare a list in python we give the list name assigned to values separated by commas.

my_list = [“item_1”, ”item_2”, ”item_3”, ”item_4”]

Similar to string indices, list indices start at 0, and lists can be sliced, concatenated and so on.

Example:

world_tour = [“Paris”, “New York”, “Melbourne”, “Swiss”]

print(type(world_tour))
print(world_tour)
print(world_tour[0])
print(world_tour[1])
print(world_tour[-1])

Note: Negative indices starts from the end of the list with index value -1.

We have several methods on lists here are few examples

stationery_list = ["Pen", "Pencil", "Notepad"]
stationery_list.append("Eraser")
# Adds new item at the end of the list
print(stationery_list)
stationery_list.insert(2, "Files")
"""
Insert method inserts a single element into a list.It takes two arguments one is 
the numerical index at which the data is to be inserted and the other is value.
"""
print(stationery_list)
stationery_list.index(“Pen”)
“””
The index method finds the given value in list and returns the index value. Generally index method is used to search where the values are incurred.
“””
These are few examples of list methods, to find out more we can use help(list) for all the list methods.

Tuples

Lists are ordered,immutable sequence of values.

Declaring tuples is similar to tuples we just enclose the values in pair of parentheses.

my_tuple = (item_1, item_2, item_3)

Tuples are immutable which means we cannot add or delete items in the tuple, and also tuples have no index methods.

Why use tuples ?
Tuples are faster than lists and safer.
Tuples are write -protected we cannot add new items once the declaration is done.
 
atmosphere = (“Oxygen”, “Hydrogen”, “Nitrogen”)
print(type(atmosphere))

Dictionary
Dictionaries are unordered set key-value pairs.The key and the value can be of different data types.Each value has a unique key which acts as an identifier for that value within the dictionary.

Defining a dictionary

my_dictionary = {‘key_1’ : ’value1’, ‘key_2’ : ‘value2’ , ‘key_3’ : ’value3’} 

Example:

code_name = { 'jack': 4098, 'sape': 4139, ‘robb’:2323}
print(type(code_name))
print(code_name)

# You can remove items in dictionary by using del keyword.

del code_name[‘sape’]
print(code_name)
You can update the values of the dictionaries by overriding them.
code_name[‘jack’] = 1212

# The len function returns the number of key-value pairs in the dictionary.
len(code_name)

Conditionals(if, elif, else)
We always need the ability to check the conditions and change the behaviour of the program accordingly. The conditional statements give us the ability, the simplest form is the ‘if’ statement.

A conditional statement tests an expression to see whether it is true or false and it does the operations based on the result.

if expression:
   statement(s)
 Note : Python must know the number of statements which must be executed when condition happens to be True.To enable this the concept of indentation occurs.All the statements below the header (if in this case) must maintain same level of indentation(4 spaces).

This concept of indentation is applied throughout Python programs.

Example:
temp.py

temperature  = 27
If temperature <=30:
	print(“Let's go to the party!”)

python3 temp.py
Let's go to the party!

If there are two possibilities of conditions then we use if, else statement.

Example:
movie_plan.py

movie_tickets = 4
if(movie_tickets >= 4):
	print(“Tickets are available, Let’s go to the movie.”)
else:
	print(“Let's have a drink, tickets are not available. ”)

python3 movie_plan.py

Multiple conditions
If we have more than two possibilities and we need more than two branches. SO we use chained conditional statements. The term elif is abbreviation of else if.There is no limit of elif statements, but the last branch has to be an else statement.
weight = float(input("Enter your weight in Kg"))
height = float(input("Enter your height in Cms"))

bmi = (weight / (height**2)) * 10000
print("Computing...")
print("Your bmi is {}\n".format(bmi))
if bmi < 18.5:
    print("Underweight")
elif 18.5 <= bmi <= 24.99:
    print("Perfect ! Normal weight")
elif 25.00 <= bmi <= 30.00:
    print("Overweight")
elif bmi > 30.00:
    print("Obese")



Part 2

Strings
In python string is a sequence of characters enclosed in either single or double quotes.
Strings are immutable sequence of Unicode points.
Creating strings in python
Example:
	name = 'Stark'
job = "CEO at Queen’s Consolidate"
print(type(name))
print(type(job))
print(name, ",", job)




Python Formatting

Using .format()

Sometimes we may want to construct strings with the value of the variable and this conceptual construction of strings is called string interpolation.

Example :

formatting.py

name = "Agent 47"
code_number = 1011010
message = "Hey {}, your code number is {}.".format(name, code_number)
print(message)







Control Flow
For-loop: 
The for loop in in Python has the ability to iterate over items of any sequence such as list or string.

It steps through the items in any ordered sequence i.e, String, List, Tuples, the keys of dictionaries and other iterable terms. The python for loop starts with a keyword for followed by a variable attribute, which will hold the values of the following sequence object, which is stepped through.

Syntax of for loop
	for variable in sequence:
		statements
Example:
colors.py

colors = ['Red', 'Black', 'Blue', 'White', 'Pink']

for color in colors:
    print(color)

python3 colors.py
```
Red
Black
Blue
White
Pink
```

5_table.py
	for index in [1, 2, 3, 4, 5]:
		print(“{} times 5 is {}”.format(index, index*5))

In this case, we just print the value in the block of statements.

python3 5_table.py
```
1 times 5 is 5
2 times 5 is 10
3 times 5 is 15
4 times 5 is 20
5 times 5 is 25
```

While Loop
A while loop statement in Python programming language repeatedly executes a target statement as long as the given condition is true. Unlike the for loop, the while loop will not run n times, but until a defined condition is met.

Syntax of While loop

while condition:
	statement(s)

Example:
	
countdown_timer.py
	
	flag = 10
    while 0 < flag:
   	        print(flag)
   	        flag = flag - 1
print("Go !!")

The Range Function

The range function in Python generates a list of numbers, which can be used to iterate over for loops and in other few cases.

Now let’s see how range function works
```
range(n)
range(begin, end)
```
range(n) generates, the integer numbers starting with 1 and ending with (n-1).
range(begin, end) generates the integer numbers starting with begin and ending with end-1.

$python3
…
...
>>> range(8)
range(0, 8)

Example: Printing the squares of numbers iterating by range function. 

square.py

for number in range(1, 7):
    square = number * number
    print(square)
Functions
Function is a block of reusable code that performs a specific task. It is a small unit of computation which may take arguments and may return values.

Note: Function body must be indented like ‘if’ statement.

Declaring a function

The keyword def introduces a function definition followed by the function name and the parenthesized list of formal parameters. The statements that form the body of the function start at the next line and must be indented.

Syntactically,

```python3
def function_name(formal parameters):
    statement(s)
```
Note: Declaring a function doesn't run the function. In order to run, you have to call the function using the function name. 

Example
```python
greet.py

# Declaring a function.
def greet():
    print("Hello ! Welcome to the party.")
# calling the function.


greet()
```

python3 greet.py
Hello ! Welcome to the party.

In this program we created a function named greet with no parameters such as empty parenthesis. The function is defined to print a string called “Hello ! Welcome to the party.”
So calling the function just prints the given string.

Functions with parameters.
A function can take parameters which are values you supply to the function so that the function can do something utilizing those. Parameters are specified within the pair of parentheses in the function definition separated by commas.

Example:

greet_names.py

def greet_name(name):
    print("Hello {}".format(name))


greet_name("Flash")
greet_name("Arrow")
greet_name("Bat")

python3 greet_names.py

Hello Flash
Hello Arrow
Hello Bat


factorial.py

def num_factorial(num):
    factorial = 1

    if num < 0:
        print("Sorry, factorial does not exist for negative numbers")
    elif num == 0:
        print("The factorial of 0 is 1")
    else:
        for i in range(1, num + 1):
            factorial = factorial * i
        print("The factorial of", num, "is", factorial)

num_factorial(5)

python3 factorial.py
The factorial of 5 is 120

# Recursion, Scope of a Variable.


Introduction to Object Oriented Python

In all the programs we wrote till now, we have designed our program around functions i.e. blocks of statements which manipulate data. This is called the procedure-oriented way of programming. There is another way of organizing your program which is to combine data and functionality and wrap it inside something called a class. This is called the object oriented programming paradigm.

A quick glance at the basics of the Object Orientation terminology.
class : A class is the blueprint from which individual objects are created. 
Object : A real World entity which have state and behavior.
Let's create a class Person with a class method say in the class.
class Person():
    def say(self):
        print("Hello")

Now let's create an object instance for the class.

class Person():
    def say(self):
        print("Hello")

jackman = Person()
jackman.say()

Extending the plot further lets us create two methods, hello and bye that take arguments.

methods_examples.py

class Person():

    def hello(self, name):
        self.name = name
        print("Hello {} How are you ?".format(self.name))

    def bye(self, name):
        self.name = name
        print("Nice Meeting You {}".format(self.name))


jackman = Person()
jackman.hello("Lee")
jackman.bye("Edison")

python3 method_examples.py

Hello lee How are you ?
Nice Meeting You edison


Note:Self is a default argument for all instance method
This needs us to repeat the instance variable for every class method instead of creating an object with the instance variables. It's now time to work with constructors.
Constructors

Constructors in Python are written under a special method __init__.

Now let us write a constructor for an object. In this, example let's create an object with instance variables name and year_of_birth.This process of writing a constructor in a class eliminates the repeating of the instance variables for every instance method.

constructors.py 
class Person():
    def __init__(self, name, year_of_birth):

        self.name = name
        self.year_of_birth = year_of_birth

    def detail(self, name):
        print("Name of the person is {}".format(name))

    def age(self, year_of_birth):
        print("Your are {} Years Old".format(year_of_birth))


person = Person('Vihar', 1998)
person.detail('Vihar')
person.age(19)

python3 constructors.py 

Name of the person is Vihar
Your are 19 Years Old


Classes and Objects Example :

class BankAccount:
    def __init__(self):
        self.balance = 0

    def withdraw(self, amount):
        self.balance -= amount
        return print(self.balance)

    def deposit(self, amount):
        self.balance += amount
        return print(self.balance)


a = BankAccount()
b = BankAccount()
a.deposit(100)
b.deposit(50)
b.withdraw(10)
a.withdraw(10)



Python3 Part 3

Errors and Exception 
The most common perspective in Python is that it handles all errors with exceptions.
An exception is a signal that an error or other unusual condition has occurred.There are several built-in exceptions, which indicates certain conditions like IndentationError: unexpected indent, ZeroDivisionError: division by zero. You can also define your exceptions.

Programs are very sensitive. It would be nice if the code always returns a valid result, but sometimes a valid result cannot be calculated.

For Example it is not possible to divide a number by zero or to access the third element in a negative item list. 

Until now error messages haven’t been more than mentioned, but if you have tried out the examples you have probably seen some. There are (at least) two distinguishable kinds of errors: 
Syntax errors
Exceptions

Syntax Errors

Syntax errors, also known as parsing errors, are perhaps the most common kind of complaint you get while you are still learning Python.Syntax errors are almost always fatal, i.e. there is almost never a way to successfully execute a piece of code containing syntax errors.

Example

	>>> print("Hello
 	 File "<stdin>", line 1
    	print("Hello
              	      ^
SyntaxError: EOL while scanning string literal
	
The error is caused by the token preceding the arrow.In this example the error is detected at print() function as the parentheses is not closed.

	
	>>> while True print("Hello World !")
  File "<stdin>", line 1
    	while True print("Hello World !")
                   	    ^
SyntaxError: invalid syntax

Since a colon ‘ : ’ is missing after the condition of while loop it encountered a syntax error.


Exceptions

Exceptions occur when exceptional situations occur in your program. For Example, what if you are going to read a file that doesn't exists or what if you accidentally deleted it when the program is running. Such situations are handled using exceptions.

Similarly, what if your program had some invalid statements ?
This is handled by Python which conveys you that there is an error.

Example : Consider a simple print function call. What if we misspelt the word print as Print ?
Note the capitalization here. In this case, Python raises a syntax error.

	>>> Print("Hello there !")
Traceback (most recent call last):
 File "<stdin>", line 1, in <module>
NameError: name 'Print' is not defined

Observer that a NameError is raised and also the location where the error was detected is printed.


	
Now let's see few types errors in Python

ZeroDivisionError : When a number is divided by zero.

>>> 2/0
Traceback (most recent call last):
  	File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
 
IndexError : When the index is out of range.

	>>> list = [1,2,3]
>>> list[4]
Traceback (most recent call last):
  	File "<stdin>", line 1, in <module>
IndexError: list index out of range

TypeError : Raised when an operation or function is applied to an object of inappropriate type
	>>> '2' + 2
Traceback (most recent call last):
 	File "<stdin>", line 1, in <module>
TypeError: must be str, not int

KeyError :  It occurs when a dictionary is incorrectly used.

	>>> dict = {'a' : 'Stark', 'b': 'Steve'}
>>> dict['c']
Traceback (most recent call last):
 File "<stdin>", line 1, in <module>
KeyError: 'c'

Exceptional Handling

Like many other programming languages, Python has exception handling. We can handle the exceptions using the try except statement. We basically put our usual statements within the try-block and keep all our error handlers in the except block.

Example: 

try:
    print(1 / 0)
except ZeroDivisionError:
    print("You can't divide by zero.")

Catching Specific Exceptions in Python

A try clause can have any number of except clause to handle them differently but only one will be executed in case an exception occurs.

We can use a tuple of values to specify multiple exceptions in an except clause. Here is an example pseudo code.

try:
   # do something
   pass

except ValueError:
   # handle ValueError exception
   pass

except (TypeError, ZeroDivisionError):
   # handle multiple exceptions
   # TypeError and ZeroDivisionError
   pass

except:
   # handle all other exceptions
   pass



Raising Exceptions

In Python programming, exceptions are raised when corresponding errors occur at run time, but we can forcefully raise it using the keyword raise.

>>> raise KeyboardInterrupt
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyboardInterrupt
>>> 

>>> raise MemoryError("Argument")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
MemoryError: Argument

raising_error.py

try:
    a = int(input("Enter a negative integer: "))
    if a >= 0:
        raise ValueError("That is not a negative number!")
except ValueError as ve:
    print(ve)

python3 raising_error.py

Enter a negative integer: 4
That is not a negative number!

try...finally

The try statement in Python can have an optional finally clause. This clause is executed no matter what, and is generally used to release external resources.




file_handling.py

try:
    f = open("test.txt", encoding='utf-8')
    # perform file operations
finally:
    f.close()

python3 file_handling.py

Modules and Packages

Modules

Python comes with hundred of modules that do all sort of things. There are also third party modules that are available for download from internet.

Python includes a set of modules called the standard library, for example math, cmath which contains mathematical functions for real and complex numbers, but there are many more.

A module is imported using the import statement.

Example :

Import module_name

Let’s now import few modules and run functions in them

>>> import math
>>> math.pi
3.141592653589793
>>> math.sin(0)
0.0
>>> math.cos(45)
0.5253219888177297

>>> import time
>>> print(time.asctime())
Thu Jul 27 01:47:01 2017

In this example we have imported time module and called asctime function from that module, which returns the current time as a String.





There is another way to import to use import statement.

>>> from time import asctime
>>> asctime()
'Thu Jul 27 01:49:10 2017'

Here, we have imported just the asctime function from the time module.

Packages

Consider a sound package, the way organize your python code creates awesome packages.

sound/                          Top-level package
      __init__.py               Initialize the sound package
      formats/                  Subpackage for file format conversions
              __init__.py
              wavread.py
              wavwrite.py
              aiffread.py
              ...
      effects/                  Subpackage for sound effects
              __init__.py
              echo.py
              surround.py
              reverse.py
              ...
      filters/                  Subpackage for filters
              __init__.py
              equalizer.py
              vocoder.py
              karaoke.py
              ...


Third party packages.
Python has got the greatest community for creating python packages. There are more than 1,00,000 packages available at https://pypi.python.org/pypi

Python package is a collection of all modules connected properly into one form and distributed PyPi, The Python Package Index maintains the list of Python packages available. Now when you are done with pip setup Go to command prompt or terminal and say

pip install <package-name>




