# Language Basics

    Welcome to this introduction on the basics of the Python language! In this mark down, we will focus on some of the foundations you will need in order to get started in Python as well as some general information that is good to know about the language. I am only going to be discussing Python 3 as Python 2 has been discontinued, but most things covered here are the same in Python 2 as they are in Python 3.

    If you are using the linux terminal to run Python files, you will want to add a shebang line (a line that tells Linux how to read the file) at the top that looks like this:

        `#!/usr/bin/env python3`

    By adding this line and running chmod on the file, you can simply run the file when you want to test it. You could also just run:

        `python3 {file_name}`

    One last thing to note is that it is standard convention to add a .py to the end of a Python file to let others know (and a Windows operating system) that the file is a Python file. There are other Python file extensions, but they will not be covered here.

## Some History On Python

    The Python language was developed in the 1980s by Guido van Rossum. The language is based off of an old language project ABC. The idea Guido van Rossum had was to create a language that was simple for users to code in and allowed for easy extensions. In the ABC language, it was difficult to add extensions to the program. 

    The other language that Python was designed along was the C language. Guido van Rossum originally intended Python to be a language used alongside C, the idea was that for a large application, you would use a language like C, but if a programmer needed to write a short shell script, Python would be the go to for writing short shell scripts. This design principle has changed over the years with more people using Python for large applications.

## What is Python? 

    - Python is an interpreted language, this means that whenever the code is translated into machine code at runtime.
    - Python is a dynamic language, meaning that variable types are only checked at the time that a line of code is executed. It also means that the variable can change types later (more on these concepts later).
    - Python is a strongly typed language, this means that the type of variables matters when performing operations on other variables (We will show this later as well).
    - Python is both an object-oriented language and a functional language.

## Python Conventions

    Here are some important conventions when coding in Python:

        - Lines of code are not terminated by a semi colon, they are terminated by a new line.
        - Different code blocks are distinguished by spaces and tabs (in general, it is a good idea to indent using spaces, since tabs are treated differently depending on the ide)
        - Hashtags denote single line comments, for multiline comments, you can use triple apostraphes to denote the start and end of a multiline comment block
        - Variable names and function names follow lowercase underscore convention, like this:
            is_correct = False
        - There are other conventions, but listing them all would take too long, but you can read more at the PeP8 site here: https://www.python.org/dev/peps/pep-0008/
        

## Data Types in Python

    All data types in Python are objects. This means that they have their own special methods that can be called on them (if you ever want to see the methods available on an object, you can call dir(`object_name`) to get a list of all of its class methods). Some of the basic types you will encounter are:

        - int: Python's integer type

        - float: Python's decimal type

        - bool: Python's boolean type (a boolean type is a True or False value)

        - str: Python's text value (keep in mind that "1" is different then 1, this is an important difference)

    Some interesting things to mention about boolean values, other data types have their own "truthy" and "falsey" values, some examples:

        False values: 0, 0.0, False, '', "", []
        True values: 20, 1.1, True, 'True', 'False'

## Variables

    Assigning variables in Python is relatively simple, all that needs to happen is putting a variable, an equals sign and some kind of value, in this format `x = 12`. Note that in Python, you do not specify the type of variable when you are declaring it, Python determines the type of variable at runtime. Two other notes:

        - As stated earlier, every type in Python is its own object.
        - Most types in Python are immutable, what happens here is that instead of changing the value contained within these variables, Python will create the new number in memory and assign the variable to the new number. This usually is not noticable in practice, but can occasionally come up with certain operations.

## Operators in Python

    Most of the operators you see in Python are the same as in other languages, but I will briefly mention all of the operators here in case these are new:
        
        + : addition operator
        - : subtraction operator
        * : multiplication operator
        % : modulo operator (retrieve the remainder of a division operation between two numbers)
        = : assignment operator
        ** : exponential operator (2 ** 3 is the same as 2*2*2)

    The division operation in Python is a bit different, there are two different operators in Python:

        / : division operator, divides the first number by the second number, even if both numbers are integers, the number returned by this operation will be a floating point number
        // : the other division operator, does the same as the above operation, except that it will also convert the output to an integer (rounds down).

    You can also do these operations in place by placing an equals sign after the operator, for example:

        2 **= 3 would be 4 (2 * 2 * 2 = 8)

    





