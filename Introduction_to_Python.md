
# Introduction to Python
Adapted from PyCharm Edu's "Introduction to Python"

----
## Ressources
- [Python Documentation](https://docs.python.org/3/index.html)

----
## Introduction

### Hello World


```python
print("Hello, world! My name is Hans")
```

    Hello, world! My name is Hans


### Comments
Comments in Python start with the hash character ( #) and include the whole line.


```python
# This is the comment for the xxx.py file
print("Hello!")  # this comment is for the second line
```

    Hello!


### Documentation string
Used for documentation
"""
This is a documentation string. It'll be available by functionName.__doc__()
"""
----
## Variables
Variable names may only contain letters, digits, and/or the underscore character, and cannot start with a digit.

### Variable definition
Variables are used to store values so we can refer to them later. A variable is like a label, and you use the ' =' symbol, known as the assignment operator, to assign a value to a variable. An assignment can be chained, e.g. a = b = 2 


```python
a = b = 2  # This is called a "chained assignment". It assigns the value 2 to variables "a" and "b".
print("a = " + str(a))
print("b = " + str(b))

greetings = "greetings"
print("greetings = " + str(greetings))
greetings = "Hello Programmer"
print("greetings = " + str(greetings))
```

    a = 2
    b = 2
    greetings = greetings
    greetings = Hello Programmer


### Undefined variable


```python
variable = 1
print(other_variable)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-47-c1a15e83013c> in <module>
          1 variable = 1
    ----> 2 print(other_variable)
    

    NameError: name 'other_variable' is not defined


### Variable types
In Python, there are two main types of numbers: integers and floats. The most important difference between them is that a float is a number that has a decimal point, and an int is a number without a decimal point.


```python
number = 9
print(type(number))   # print type of variable "number"

float_number = 9.0
print(type(float_number))
```

    <class 'int'>
    <class 'float'>


### Type conversion
There are several built-in functions that let you convert one data type to another. These functions return a new object representing the converted value. int(x) converts x to an integer. float(x) converts x to a floating-point number. str(x) converts object x to a string representation. 


```python
number = 9
print(type(number))   # print type of variable "number"

float_number = 9.0
print(float_number)
print(int(float_number))
```

    <class 'int'>
    9.0
    9


### Arithmetic operators
Just as with any other programming language, the addition ( +), subtraction ( -), multiplication ( \*), and division ( /) operators can be used with numbers. In addition Python has the power ( \*\*) and modulo ( %) operators. 


```python
number = 9.0        # float number

result = number/2

remainder = number%2

print("result = " + str(result))
print("remainder = " + str(remainder))
```

    result = 4.5
    remainder = 1.0


### Assignements
Augmented assignment is a single statement combining a binary operation and an assignment statement such as +=, -=, etc. 


```python
number = 9.0
print("number = " + str(number))

number -= 2
print("number = " + str(number))

number += 5

print("number = " + str(number))

```

    number = 9.0
    number = 7.0
    number = 12.0


### Boolean operators
Boolean is a type of value that can only be True or False. The == (equality) operator checks whether the two variables being compared are equal.


```python
two = 2
three = 3

is_equal = two == three

print(is_equal)
```

    False


### Comparison operators
Python has many types of comparison operators including >=, <=, >, <, etc. All comparison operations in Python have the same priority. Comparisons yield boolean values: either True or False. Comparisons can be chained arbitrarily. 


```python
one = 1
two = 2
three = 3

print(one < two < three)  # This chained comparison means that the (one < two) and (two < three) comparisons are performed at the same time.

is_greater = three > two
print(is_greater)
```

    True
    True


----
## Strings

### Concatenation
Combining two strings using the + symbol is called concatenation. 


```python
hello = "Hello"
world = 'World'

hello_world = hello + " " + world
print(hello_world)
```

    Hello World


### String multiplication
Python supports a string-by-number multiplication (but not the other way around!).


```python
hello = "hello"
ten_of_hellos = hello * 10
print(ten_of_hellos)
```

    hellohellohellohellohellohellohellohellohellohello


### String indexing
You can access a character of a string if you know its position. For example, str[index] will yield the character at position index in the string str. 
Note that string index always starts at 0. 
Indices may also be negative numbers, to start counting from the right. Note that since -0 is the same as 0, negative indices start from -1.


```python
python = "Python"
print("h " + python[3])

p_letter = python[0]
print(p_letter)
```

    h h
    P


### String negative indexing
You can use negative numbers in the indexing operator to count characters ‘backwards’ from the end of the string.


```python
long_string = "This is a very long string!"
exclamation = long_string[-1]
print(exclamation)
```

    !


### String slicing
Slicing is used to get multiple characters (a substring) from a string. Its syntax is similar to that of indexing, but instead of just one index you use two indices (numbers) separated by a colon, e.g. str[ind1:ind2].
<br/>
**Example:** 
- str[start:end] \# items start through end-1
- str[start:]    \# items start through the rest of the array
- str[:end]      \# items from the beginning through end-1
- str[:]         \# a copy of the whole array


```python
monty_python = "Monty Python"
monty = monty_python[:5]      # one or both index could be dropped. monty_python[:5] is equal to monty_python[0:5]
print(monty)
python = monty_python[6:]
print(python)
```

    Monty
    Python


### In operator
If you want to check whether a string contains a specific letter or a substring, you can use the in keyword. 


```python
ice_cream = "ice cream"
print("cream" in ice_cream)    # print boolean result directly

contains = "cream" in ice_cream
print(contains)
```

    True
    True


### String length
The len() function is used to count how many characters a string contains.


```python
phrase = """
It is a really long string
triple-quoted strings are used
to define multi-line strings
"""
first_half = phrase[:int(len(phrase)/2)]
print(first_half)
```

    
    It is a really long string
    triple-quoted st


### Character escaping
Backslash is used to escape single or double quotation marks, for example 'It\'s me' or "She said \"Hello\"". The special symbol '\n' is used to add a line break to a string. 
Single quotation mark could be used in double quoted string without escaping and vice versa. 


```python
dont_worry = "Don't worry about apostrophes"
print(dont_worry)
print("\"Sweet\" is an ice-cream")
print('The name of this ice-cream is "Sweet\'n\'Tasty" ')
```

    Don't worry about apostrophes
    "Sweet" is an ice-cream
    The name of this ice-cream is "Sweet'n'Tasty" 


### Basic string methods
There are a lot of useful string methods. You can use the lower() method to get rid of any capitalization in your strings. The upper() method is used to make a string uppercase. To call any string method, type a dot after the string (or a variable containing the string) and the method name after it, e.g. "John".upper().


```python
monty_python = "Monty Python"
print(monty_python)

print(monty_python.lower())    # print lower-cased version of the string

print(monty_python.upper())    # print upper-cased version of the string
```

    Monty Python
    monty python
    MONTY PYTHON


### String formatting
The % operator after a string is used to combine a string with variables. The % operator will replace %s in a string with the string variable that comes after it. The %d special symbol is used as a placeholder for numeric or decimal values. 


```python
name = "John"
print("Hello, Reader! My name is %s!" % name)     # Note: %s is inside the string, % is after the string

years = 28
print("I'm %d years old" % years)
```

    Hello, Reader! My name is John!
    I'm 28 years old


----
## Datastructures


### List introduction
A list is a data structure you can use to store a collection of different pieces of information under a single variable name. A list can be written as an array of comma-separated values (items) between square brackets, e.g. lst = [item1, item2]. Lists might contain items of different types, but usually all the items in the list are of the same type. Like strings, lists can be indexed and sliced (see [String slicing](#string-slicing)).


```python
squares = [1, 4, 9, 16, 25]   # create new list
print(squares)

print(squares[1:4])
```

    [1, 4, 9, 16, 25]
    [4, 9, 16]


### List operations
You can add new items at the end of the list, by using the append() method and concatenation. Unlike strings, lists are a mutable type, i.e. it is possible to change their content using lst[index] = new_item 


```python
animals = ['elephant', 'lion', 'tiger', "giraffe"]  # create new list
print(animals)

animals += ["monkey", 'dog']    # add two items to the list
print(animals)

animals.append("dino")   # add one more item to the list using append() method
print(animals)

animals[-1] = "dinosaur"
print(animals)
```

    ['elephant', 'lion', 'tiger', 'giraffe']
    ['elephant', 'lion', 'tiger', 'giraffe', 'monkey', 'dog']
    ['elephant', 'lion', 'tiger', 'giraffe', 'monkey', 'dog', 'dino']
    ['elephant', 'lion', 'tiger', 'giraffe', 'monkey', 'dog', 'dinosaur']


### List items
Assignment to slices is also possible, and this can even change the size of a list or clear it entirely. 


```python
animals = ['elephant', 'lion', 'tiger', "giraffe", "monkey", 'dog']   # create new list
print(animals)

animals[1:3] = ['cat']    # replace 2 items -- 'lion' and 'tiger' with one item -- 'cat'
print(animals)

animals[1:3] = []     # remove 2 items -- 'cat' and 'giraffe' from the list
print(animals)

animals = []
print(animals)
```

    ['elephant', 'lion', 'tiger', 'giraffe', 'monkey', 'dog']
    ['elephant', 'cat', 'giraffe', 'monkey', 'dog']
    ['elephant', 'monkey', 'dog']
    []


### Tuples
Tuples are almost identical to lists. The only significant difference between tuples and lists is that tuples cannot be changed: you cannot add, change, or delete elements from the tuple. Tuples are constructed by a comma operator enclosed in parentheses, for example (a, b, c). A single item tuple must have a trailing comma, such as (d,). 


```python
alphabet = ('a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o',
            'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z')

print(len(alphabet))
```

    26


### Dictionaries
A dictionary is similar to a list, except that you access its values by looking up a key instead of an index. A key can be any string or a number. Dictionaries are enclosed in curly braces e.g. dct = {'key1' : "value1", 'key2' : "value2"}. 


```python
# create new dictionary.
phone_book = {"John": 123, "Jane": 234, "Jerard": 345}    # "John", "Jane" and "Jerard" are keys and numbers are values
print(phone_book)

# Add new item to the dictionary
phone_book["Jill"] = 345
print(phone_book)

# Remove key-value pair from phone_book
del phone_book['John']

print(phone_book["Jane"])
```

    {'John': 123, 'Jane': 234, 'Jerard': 345}
    {'John': 123, 'Jane': 234, 'Jerard': 345, 'Jill': 345}
    234


### Dictionaries keys() and values()
There are a lot of useful methods in dictionaries such as keys() and values(). 


```python
phone_book = {"John": 123, "Jane": 234, "Jerard": 345}  # create new dictionary
print(phone_book)

# Add new item to the dictionary
phone_book["Jill"] = 456
print(phone_book)

print(phone_book.keys())

print(phone_book.values())
```

    {'John': 123, 'Jane': 234, 'Jerard': 345}
    {'John': 123, 'Jane': 234, 'Jerard': 345, 'Jill': 456}
    dict_keys(['John', 'Jane', 'Jerard', 'Jill'])
    dict_values([123, 234, 345, 456])


### In keyword
The in keyword is used to check if a list or a dictionary contains a specific item. You can apply in to lists or dictionaries the same way as you did with strings. 


```python
grocery_list = ["fish", "tomato", 'apples']   # create new list

print("tomato" in grocery_list)    # check that grocery_list contains "tomato" item

grocery_dict = {"fish": 1, "tomato": 6, 'apples': 3}   # create new dictionary

print('fish' in grocery_dict.keys())
```

    True
    True


----
## Conditions expressions

### Boolean operators
Boolean operators compare statements and return results in boolean values. The boolean operator **and** returns *True* when the expressions on both sides of **and** are *True*. The boolean operator **or** returns *True* when at least one expression on either side of **or** is *True*. The boolean operator **not** inverts the boolean expression it precedes. 


```python
name = "John"
age = 17

print(name == "John" or age == 17)    # checks that either name equals to "John" OR age equals to 17

print(name == "John" and age != 23)
```

    True
    True


### Boolean operators order
Boolean operators are not evaluated from left to right. There's an order of operations for boolean operators: not is evaluated first, and is evaluated next, or is evaluated last. 


```python
name = "John"
age = 17

print(name == "John" or not age > 17)

print(name == "John" or not age > 17)

print(name == "Ellis" or not name == "John" and age == 17 )
```

    True
    True
    False


### If statement
The if keyword is used to form a conditional statement that executes some specified code after checking if its expression is True. Python uses indentation to define code blocks. 


```python
name = "John"
age = 17

if name == "John" or age == 17:   # check that name is "John" or age is 17. If so print next 2 lines.
    print("name is John")
    print("John is 17 years old")

tasks = ['task1', 'task2']    # create new list

if len(tasks) != 0:
    print("not empty")
```

    name is John
    John is 17 years old
    not empty


### Else, elif part in if statement
The else statement complements the if statement. The elif keyword is short for "else if". 


```python
x = 28

if x < 0:
    print('x < 0')                      # executes only if x < 0
elif x == 0:
    print('x is zero')                 # if it's not true that x < 0, check if x == 0
elif x == 1:
    print('x == 1')                    # if it's not true that x < 0 and x != 0, check if x == 1
else:
    print('non of the above is true')

name = "John"

if name == "John":
    print(True)
else:
    print(False)
```

    non of the above is true
    True


----
## Loops

### For loops
for loops are used to iterate over a given sequence. On each iteration, the variable defined in the for loop will be assigned to the next value in the list. 


```python
for i in range(5):    # for each number i in range 0-4. range(5) function returns list [0, 1, 2, 3, 4]
    print(i)          # this line is executed 5 times. First time i equals 0, then 1, ...


primes = [2, 3, 5, 7]   # create new list

for prime in primes:
    print(prime)
```

    0
    1
    2
    3
    4
    2
    3
    5
    7


### For loop using string
Strings are very similar to lists in Python. You can use string to iterate over it. 


```python
hello_world = "Hello, World!"

for ch in hello_world:    # print each character from hello_world
    print(ch)

length = 0      # initialize length variable

for ch in hello_world:
    length += 1     # add 1 to the length on each iteration

print(len(hello_world) == length)
```

    H
    e
    l
    l
    o
    ,
     
    W
    o
    r
    l
    d
    !
    True


### While loop
A while loop is similar to an if statement: it executes some code if some condition is true. The key difference is that it will continue to execute indented code for as long as the condition is True. 


```python
square = 1

while square <= 10:
    print(square)    # This code is executed 10 times
    square += 1      # This code is executed 10 times

print("Finished")  # This code is executed once

square = 0
number = 1

while number < 10:
    square = number ** 2
    print(square)
    number += 1
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    Finished
    1
    4
    9
    16
    25
    36
    49
    64
    81


### Break keyword
An infinite loop is a loop that never exits. If the loop condition happens to always be True, such a loop becomes infinite. The break keyword is used to exit the current loop. 


```python
count = 0

while True:  # this condition cannot possibly be false
    print(count)
    count += 1
    if count >= 5:
        break           # exit loop if count >= 5


zoo = ["lion", 'tiger', 'elephant']
while True:                         # this condition cannot possibly be false
    animal = zoo.pop()       # extract one element from the list end
    print(animal)
    if animal == "elephant":
        break           # exit loop
```

    0
    1
    2
    3
    4
    elephant


### Continue keyword
The continue keyword is used to skip the rest of the code inside the loop for the currently executed loop and return to the for or while statement. 


```python
for i in range(5):
    if i == 3:
        continue   # skip the rest of the code inside loop for current i value
    print(i)

for x in range(10):
    if x % 2 == 0:
        continue   # skip print(x) for this loop
    print(x)
```

    0
    1
    2
    4
    1
    3
    5
    7
    9


----
## Functions

### Definition
Functions are a convenient way to divide your code into useful blocks, make it more readable and help reuse it. Functions are defined using the keyword def, followed by the function's name. 


```python
def hello_world():  # function named my_function
    """This is documentation string for function. It'll be available by hello_world.__doc__()"""
    print("Hello, World!")

for i in range(5):
    hello_world()   # call function defined above 5 times
```

    Hello, World!
    Hello, World!
    Hello, World!
    Hello, World!
    Hello, World!


### Parameters and call arguments
Function parameters are defined inside the parentheses (), following the function name. A parameter acts as a variable name for the passed argument.


```python
def foo(x):                 # x is a function parameter
    print("x = " + str(x))

foo(5)   # pass 5 to foo(). Here 5 is an argument passed to function foo.

def square(x):
    print(x ** 2)

square(4)
square(8)
```

    x = 5
    16
    64


### Return value
Functions may return a value to the caller, using the keyword return. You can use the returned value to assign it to a variable or just print it out.


```python
def sum_two_numbers(a, b):
    return a + b            # return result to the function caller

c = sum_two_numbers(3, 12)  # assign result of function execution to variable 'c'


def fib(n):
    result = []
    a = 1
    b = 1
    while a < n:
        result.append(a)
        tmp_var = b
        b += a
        a = tmp_var
    return result

print(fib(10))
```

    [1, 1, 2, 3, 5, 8]


### Default parameters
Sometimes it's useful to specify a default value for one or more function parameters. This creates a function that can be called with fewer arguments than it is defined to allow.


```python
def multiply_by(a, b=2):
    return a * b

print(multiply_by(3, 47))
print(multiply_by(3))    # call function using default value for b parameter


def hello(subject, name="Hans"):
    print("Hello %s! My name is %s" % (subject, name))

hello("Programmer", "Jane")    # call 'hello' function with "PyCharm as a subject parameter and "Jane" as a name
hello("Programmer")            # call 'hello' function with "PyCharm as a subject parameter and default value for the name
```

    141
    6
    Hello Programmer! My name is Jane
    Hello Programmer! My name is Hans


### Lambdas
A lambda function is a small anonymous function which can take any number of arguments, but can only have one expression.
Lambda functions are used when an anonymous function is required for a short period of time.


```python
x = lambda a : a + 10
print(x(5))

x = lambda a, b : a * b
print(x(5, 6))


def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)
mytripler = myfunc(3)

print(mydoubler(11)) 
print(mytripler(11))
```

    15
    30
    22
    33


----
## Classes and objects
[Python Documentation](https://docs.python.org/3/tutorial/classes.html)

### Definition
An object combines variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially templates for creating your objects. You can think of an object as a single data structure that contains data as well as functions. Functions of objects are called methods. 


```python
class MyClass:
    variable = "object variable"

    def foo(self):   # we'll explain self parameter later in task 4
        print("Hello from function foo")

my_object = MyClass()  # variable "my_object" holds an object of the class "MyClass" that contains the variable and the "foo" function
```

### Variable access
To access a variable inside an object, see example below. You can change the values of variables defined in a class for different instances (objects) of this class.


```python
class Car:
    color = ""
    def description(self):
        description_string = "This is a %s car." % self.color    # we'll explain self parameter later in task 4
        return description_string

car1 = Car()
car2 = Car()

car1.color = "blue"
car2.color = "red"
print(car1.color)
print(car2.color)
print(car1.description())
print(car2.description())
```

    blue
    red
    This is a blue car.
    This is a red car.


### Self explanation
It's time to explain the self parameter used in previous tasks. The self parameter is a Python convention. self is the first parameter passed to any class method. Python will use the self parameter to refer to the object being created.


```python
class Complex:
    def create(self, real_part, imag_part):
        self.r = real_part
        self.i = imag_part

class Calculator:
    current = 0

    def add(self, amount):
        self += amount
    def get_current(self):
        return self.current
```

### Special \_\_init\_\_ method
*\_\_init\_\_* function is used to initialize the objects it creates. *\_\_init\_\_* is short for "initialize". *\_\_init\_\_*() always takes at least one argument, self, which refers to the object being created. *\_\_init\_\_*() function sets up each object the class creates. 


```python
class Square:

    def __init__(self):    # special method __init__
        self.sides = 4

square = Square()
print(square.sides)

class Car:
    def __init__(self, color):
        self.color = color

car = Car("blue")    # Note: you should not pass self parameter explicitly, only color parameter

print(car.color)
```

    4
    blue


----
## Modules and packages
[Python Documentation](https://docs.python.org/3/tutorial/modules.html)

### Import module
Modules in Python are simply Python files with the .py extension containing Python definitions and statements. Modules can be handy when you want to use your function in a number of programs without copying its definition into each program. Modules are imported from other modules using the import keyword and the file name without an extension. The first time a module is loaded into a running Python script, it is initialized by executing the code in the module once.
</br>
If the Modules aren't located in the root directory or are defined in the PythonPath we have tell Python were to find it. The variable sys.path is a list of strings that determines the interpreter’s search path for modules. It is initialized to a default path taken from the environment variable PYTHONPATH, or from a built-in default if PYTHONPATH is not set. 


```python
#res/Introduction_to_Python/calculator.py 
#res/Introduction_to_Python/my_module.py

#imports.py
import sys
sys.path.append('res/Introduction_to_Python') # here we add the folder with modules to the PYTHONPATH variable
                  
import calculator

calc = calculator.Calculator()    # create new instance of Calculator class defined in calculator module
calc.add(2)
print(calc.get_current())

import my_module

my_module.hello_world()
```

    2





    'Hello, World!'



### From import
One form of the import statement imports names from a module directly into the importing module's symbol table. This way you can use the imported name directly without the module_name prefix.


```python
#res/Introduction_to_Python/calculator.py 
#res/Introduction_to_Python/my_module.py

#imports.py
import sys
sys.path.append('res/Introduction_to_Python') # here we add the folder with modules to the PYTHONPATH variable

from calculator import Calculator

calc = Calculator()    # here we can use Calculator class directly without prefix calculator.
calc.add(2)
print(calc.get_current())

from my_module import hello_world

print(hello_world())    # Note: hello_world function used without prefix

```

    2
    Hello, World!


### Builtin modules
Python comes with a library of standard modules.


```python
import datetime

print(datetime.datetime.today())
```

    2019-02-07 20:26:10.649112


----
## File input/output
[Python Documentation](https://docs.python.org/3/tutorial/inputoutput.html)

### Read file
Python has a number of built-in functions to read and write information from a file on your computer. The open function is used to open a file. The file can be opened in read mode (using "r" as the second argument) or in write mode (using "w" as the second argument). The open function returns the file object. You need to store it to close the file later. 


```python
f = open("res/Introduction_to_Python/input.txt", "r")   # here we open file "input.txt". Second argument used to identify that we want to read file
                             # Note: if you want to write to the file use "w" as second argument
for line in f.readlines():   # read lines
    print(line)
f.close()                   # It's important to close the file to free up any system resources.

f1 = open("res/Introduction_to_Python/input1.txt", "r")
print(f1.readline())
f1.close()
```

    I am a temporary file. Maybe someday, I'll become a real file.
    My first line
    


### Write to file
If you open a file using "w" (write) as the second argument, a new empty file will be created. Note that if another file with the same name exists, it will be deleted. If you want to add some content to an existing file, you should use the "a" (append) modifier.


```python
zoo = ['lion', "elephant", 'monkey']

if __name__ == "__main__":
    f = open("res/Introduction_to_Python/output.txt", "a")

    for i in zoo:
        f.write(i + ",")

    f.close()
```
