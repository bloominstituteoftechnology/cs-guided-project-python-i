# CS Fundamentals in Python - Python I

This is the starter code for Computer Science - Sprint 1: CS Fundamentals in Python - Module 1: Python I.

Please fork and clone this repo to your computer by the start of class.
Objectives
create a simple Python program that utilizes the basic types and data structures, uses correct syntax throughout, and employs conditionals and loops
compare and contrast the characteristics of Lists, Tuples, Sets, and Dictionaries in Python
write Python code that shows the ability to perform operations on each Lists, Dictionaries, Tuples, and Sets
Introduction
In this project, you will write a series of "toy programs" in Python designed to quickly get you comfortable with the features and syntax of the Python programming language.

Why are you working on this project? Throughout the rest of the Computer Science curriculum, we will be writing all of our code in Python. You need to get up to speed and comfortable writing in Python as quickly as possible. Writing "toy programs" is one of the easiest and quickest ways to get comfortable with a new language. Also, to solve the challenges, you will likely need to practice your debugging, problem-solving, and research skills. All of these skills are crucial to your continued success during your time working in the Computer Science curriculum. These skills are also necessary for you to excel as a professional developer.

Imagine that "future you" is working as a paid developer. Imagine that your team comes to you with a difficult problem to solve. The project that you will be working with is in a language that you do not know well. What would you do? Hopefully, you would have the necessary problem-solving, research, and planning skills to quickly get up to speed with the new language so you can tackle the task. This project gives you a chance to practice that scenario.

Instructions and/or completion requirements
Inside the src/ directory, you will find a series of Python files. Each file contains a few topical exercises that will allow you to practice learning a fundamental aspect of the Python programming language.

The files numbered 00 - 10 are mandatory (the files numbered 11 - 15 are part of the stretch goals for this module project).

The suggested order for going through each of the directories is:

 00_hello.py -- Hello world
 01_bignum.py -- Print some big numbers
 02_datatypes.py -- Experiment with type conversion
 03_modules.py -- Learn to import from modules
 04_printing.py -- Formatted print output
 05_lists.py -- Python's version of arrays
 06_tuples.py -- Immutable lists typically for heterogenous data
 07_slices.py -- Accessing parts of lists
 08_comprehensions.py -- List comprehensions
 09_dictionaries.py -- Dictionaries
 10_functions.py -- Functions
Resources
Installing Python and pipenv
JavaScript <-> Python cheatsheet
How to read Specs and Code
Python 3 standard library
Stretch goals
After completing the files 00 through 10, you can attempt to tackle the following problems as stretch goals:

 11_args.py -- Arguments and Keyword Arguments
 12_scopes.py -- Global, Local, and Non-Local scope
 13_file_io.py -- Read and write from files
 14_cal.py -- Experiment with module imports and implement a text-based calendar
 15_classes.py -- Classes and objects
After completing all the files, here are some additional stretch goals you can focus on:

 One of Python's central philosophical tenets is its emphasis on readability. To that end, the Python community has standardized around a style guide called PEP 8. Take a look at it and then go over the code you've written and make sure it adheres to what PEP 8 recommends. Alternatively, PEP 8 linters exist for most code editors (you can find instructions on installing a Python linter for VSCode here). Try installing one for your editor!
 Rewrite code challenges you've solved before or projects you've implemented before in a different language in Python. Start getting in as much practice with the language as possible!
 Write a program to determine if a number, given on the command line, is prime.
 After writing a first-pass solution, work on optimizing your original solution by implementing The Sieve of Eratosthenes, one of the oldest algorithms known (ca. 200 BC).
Tests
This module project does not include any test files.

FAQs
Why is the '+' operator being used to concatenate strings? I thought we were supposed to use the join() method in Python?
Using join() to join large numbers of strings is faster in Python than using the + operator. The reason is that every time you join() or use the + operator, a new string is created. So if you only have to join() once, versus using + hundreds of times, you'll run faster.

If you want to use the join() approach, you'll have to have all your strings in a list, which employs more memory than just having the two or three that you need at a time to use +. So there's a tradeoff.

Another tradeoff might be in readability. It is likely more natural to read the + version. That's worth something.

Finally, if + is fast enough for this case, it might not be worth the time to bother making a list of strings to join().

Speed comparison with different ways of concatenating strings
How do you get out of the Python built-in help?
Hit q for "quit".

It's a standard command in Unix "pagers" (programs that show documents a page at a time).

Are there any helpful VS Code extensions that you recommend for using with Python?
Official VS Code Python Extension
I'm on Windows; what command do I use to run Python?
If you're running in PowerShell or cmd, use:

py
If in bash, use python or python3.

What version of Python do I need?
You should have version 3.7 or higher. Test with:

python --version
Do I need to use pipenv?
You should. Good Python devs know how to use pipenv.

How do I get out of the Python REPL?
Hit CTRL-D; this is the way End-Of-File is signified in Unix-likes.

What does "REPL" mean?
Read, Evaluate, Print Loop.

It reads your input, evaluates it, and prints the result. And loops.

I'm on a Mac, and when I run Python it says I'm on version 2.7. Why?
Macs come with version 2.7 by default. You'll need to install version 3.

And preferably use pipenv after that.

Does Python use tabs or spaces?
PEP 8 says four spaces.

How do I convert an iterator into a list?
Cast it:

list(range(5))
produces:

[0, 1, 2, 3, 4]
Does Python have hoisting?
No.

What is hoisting?
Does scoping work similar to other languages?
Generally, and also not really. Variables are either global or function-local.

Since there are no declarations, there's no block-level scope.

It is similar to var in JavaScript.

Can you return a reference to a function from another function? Or store it in a variable?
Yes. Functions are first-class citizens.

Can you use boolean shortcut assignments?
Yes, you can, this is common in Perl and JavaScript, but it's not particularly idiomatic in Python.

x = SomethingFalsey or 5
Can you do anonymous functions?
You can use lambda for simple functions:

adder = lambda x, y: x + y

adder(4, 5)   # 9

do_some_math(4, 5, lambda x, y: y - x)
Is a dict like a JavaScript object?
Sort of.

The syntax is different, though. In Python you must use [] notation to access elements. And you must use " around the key names.

What are all those method names with double underscores around them?
Those are functions you typically don't need to use but can override or call if you wish.

Most commonly used are:

__init__() is the constructor for objects
__str__() returns a string representation of the object
__repr__() returns a string representation of the object, for debugging
How do I get a value from a dict?
d = {
    "a": 2,
    "b": 3
}

print(d["a"])
You don't use dot notation.

When do we run pipenv shell?
pipenv shell puts you into your work environment. When you're ready to work, or run the code, or install new dependencies, you should be in your pipenv shell.

How do I get out of the pipenv shell?
Type exit.

How do I install additional packages from pipenv?
pipenv install packagename
Is it possible to use system-wide packages from inside the virtual environment?
This is not recommended.

Where are good Python docs?
Official documentation tutorial and library reference.
The official docs might be hard to read at first, but you'll quickly get used to them.

Which linter?
Pylint or Flake8. The latter seems to be a bit more popular.

Can you dynamically add new methods/properties to class through other functions? Or must all properties/methods be declared at once?
You can add them dynamically at runtime, but you have to add them to the class itself:

class Foo():
    pass

f = Foo()

Foo.x = 12  # Dynamically add property to class

f.x == 12 # True!

def a_method(self):
    print("Hi")

Foo.hi = a_method  # Dynamically add method to class

f.hi()   # Prints "Hi"
The above example is not a common thing to see in Python, however.

Following this flow: 1) class Dog is created with attributes size and weight. 2) A new instance called Snoopy of class Dog is created. 3) Class Dog gets the method bark() dynamically added to it. Question: will Snoopy now have access to the bark() method?
Yes.

If a subclass inherits from two superclasses with a method of the same name, which method will the subclass use?
The answer to this is twofold:

Lots of devs and shops frown on multiple inheritance, so maybe just don't do it. (Discussion)

As for the order in which methods of the same name are resolved, check out the MRO Algorithm, which is what Python uses.

How to handle multiple inheritance and why/when to do it in the first place?
class Base1:
    pass

class Base2:
    pass

class Derived(Base1, Base2):  # Multiple inheritance
    pass
Sometimes multiple inheritance can lead to elegant solutions when a subclass needs attributes from multiple, otherwise-unrelated parent classes.

However, a lot of people find it's not worth the trouble) and opt for other solutions, like composition.

Why use tuples instead of lists?
Tuples are immutable. There's a school of thought that says bugs can be reduced if you make as many things immutable as you can.
Tuples are faster than lists to access.
Some tuples (containing primitive types), can be used as dict keys.
What's the difference between repr and str?
Generally speaking, __repr__ is the string a dev would want to see if they dumped an object to the screen. __str__ is the string a user would want to see if the object were print()ed.

The output of __repr__ should be valid Python code that can reproduce the object.

class Goat:
    def __init__(self, leg_count):
        self.leg_count = leg_count

    def __repr__(self):
        return f'Goat(leg_count={self.leg_count})'

    def __str__(self):
        return f'a goat with {self.leg_count} legs'
In action:

>>> g = Goat(4)
>>> str(g)
'a goat with 4 legs'
>>> g
Goat(leg_count=4)
>>> Goat(leg_count=4)  # output of __repr__ makes a clone of that object!
Goat(leg_count=4)
How does sys.argv work?
It's a list that holds command line arguments. It is a way for a user to run your program and specify different behavior from the command line.

Here's a small program that prints the command line arguments:

import sys

for i in range(len(sys.argv)):
    print(f'Argument #{i} is: {sys.argv[i]}')
and here's some output, assuming you named the script foo.py:

$ python foo.py
Argument #0 is: foo.py
$ python foo.py antelope buffalo
Argument #0 is: foo.py
Argument #1 is: antelope
Argument #2 is: buffalo
Note that the 0th element in the list is the name of the program.

Here's another program that prints up to whatever number the user specifies:

import sys

for i in range(int(sys.argv[1])):
    print(i+1)
Example runs:

$ Python foo.py 2
1
2
$ Python foo.py 4
1
2
3
4
How do I concatenate two arrays into a single array?
Use extend().

a = [1, 2, 3]
b = [4, 5, 6]

a.extend(b)

print(a)   # [ 1, 2, 3, 4, 5, 6 ]
What are some ways to learn a new language?
Figure out how variables and functions work.
Build small toy programs to test individual features.
Build a larger project that exercises many features.
Don't get frustrated! Treat the problem like a curiosity, a thing to be studied.
Do small tutorials or code-alongs.
Find docs you like.
Learn the differences between this language and one you know.
Learn this language's way of doing the things you know.
Things to look for in the new language:

Collections (arrays, vectors, dictionaries)
Data types
Iterators
Flow control (if, while, loops, etc.)
Functions
etc.
Why test code frequently?
It's often better to make progress in small increments than to write a bunch of stuff and test it in one go.

Also, it's easier to stay motivated if you spend 10 minutes getting a first version going, even if it's missing 99% of its features, and then starting to iterate.

Why isn't official documentation more helpful than Stack Overflow?
Often official documentation is more geared toward being a concise reference.

Stack Overflow is more of an example-based learning environment.

Sometimes you need to know the specific details. In those cases, you can dig into the spec, with all its lawyerly language, and try to decipher what it is you have to do.

Other times, you just need a getting-started example, and Stack Overflow is great for that.

Both types of documentation have their purpose.

During an interview, what do I do if I can't remember the exact syntax?
Just say so.

"I can't remember how to add an element to the end of the list in Python... is it push()? In any case, we'll call the function here that does that."

(It turns out it's append() in Python, but being honest and describing what you're trying to do will get you 99% of the way there in an interview.)