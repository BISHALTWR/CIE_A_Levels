# How to prepare for your exams using this note?

## Install required things

- Install `python`(from python.org or microsoft store)
- Install jupyter notebook or `Jupyter extension` in Vs Code
- Create a new notebook file with extension `.ipynb`

> You can use `.py` file too but I recommend notebook files.

## Learning

- Read the text and description properly
- Copy (or better type) the codes and run them yourself
- Make changes to code, predict the output and run to see actual output
    - If you were right and you are able to give reasons too, good
    - Else, review the concepts again

> Documentation, google and chatGpt are really helpful when you get stuck. (Prioritise in that order when you are learning)

> Don't skip topics when studying for the first time.

---
---

# Introduction

- Python is an object-oriented programming language used mostly for data science but also in web development, automation and more.

## Writing good codes
- Pythonic code: Code that takes advantage of features of python and widely accepted design principles.

- Try running this:
```py
import this
```

- Output will be:
```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

- Its good to keep these in mind (I don't mean remember) these `guidelines` for writing good code.

---

## Variables, Assignment and operations

- `Variables` are entities whose values can be changed. (They are just location in memory).
- Names given to *things in python are called `identifiers`.
- `Assignment` sets value of variables.

```py
x = 5 # Here x is identifier for variable whose value is assigned to 5
print(x) # This outputs 5 when you run this since value of x is 5
```

## Data type

> What types of values can you assign to variable?

- In some other langugages, you need to declare the variable along with its data type, such languages are `statically typed`.
- Python is `dynamically typed` that means we don't have to specify (and set) type of value that variable can hold. 
- However, this doesn't mean that python doesn't have data type. 

- Python has many built-in data types and you can also create your own class(which is *like custom data type).

- Try running this:
```py
x = 5
print(type(x))

print(type(1.5))

print(type('x'))

print(type([1,2,3,4]))

print(type((1,2,3,4)))
```

- Output
```py
<class 'int'>
<class 'float'>
<class 'str'>
<class 'list'>
<class 'tuple'>
```

> Python has other types too but you don't need to remember all of them for your exams. Google them if you want.

> Everything in python is a class. This will be elaborated later (or search it if you are curious).

- Operators in python:
    - Arithmetic
    - Relational
    - Logical ...

- Run this:
```py
x = 7
y = 2

print(x + y) #Addition
print(x - y) #Subtraction
print(x * y) #Multiplication
print(x / y) #Division
print(x // y) #Floor division
print(x ** y) #Exponential
print(x % 2) #Remainder(Modulus)
```
---

## Input and output

- You have already seen `print()` function before. It outputs content.

- Run this:
```py
x = "Bishal"

print('x') # Values enclosed in inverted commas are printed as is.
print(x) # If not enclosed in inverted commas, value associated with the identifier is displays. 

print('x is:',x) # You can combine bothExponential

# I highly recommend f string
print(f"x is: {x}.") # Notice the f at start. Things inside `{}` are treated as identifier and rest as string 
```

- Output will be:
```markdown
x
Bishal
x is: Bishal
x is: Bishal.
```

- To take input, you can use `input()` function

- Run this:
```py
x = input("Enter your name: ") # You will be prompted and the value you enter will be assigned to x
print(f"Your name is: {x}") # This displays what you entered
```

- You can use escape sequence to escape the default behavior of special characters.
```py
print("Line will be changed after this.\nThis is a new line.")
print('This inserts horizontal tab\there\tand here\t.')
print("You can display \" like this.")
```

- Python also has triple quoted strings that are displayed as they are:
```py
print('''
This is shown
as it is 
written here.
''')
```

- `sep` and `end`
```py
print("Hello","this","is","a","sentence.")
print("This","is","another","sentence.")

# If you print the sentences above, you get two sentences in separate line, and each word is separated by a space. i.e. default: sep = ' ' and end = '\n'.

# You can modify sep(separator) and end(ending) like this.

print("Hello","this","is","a","sentence.", sep="_", end="...") # Use _ for separating values and end with ... 
print("This","is","another","sentence.")

# But that only works for that specific print statement
```
---

## Conditional/Branching

> These statements let you run different lines of code based on some condition.
- Python has two:
    - `if elif... else`
    - `match case`

- Run this:
```py
x = int(input("Enter a number: "))

if x > 0:
    print(f"{x} is positive.")
elif x < 0:
    print(f"{x} is negative.")
else: # in every other case
    print(f"{x} is zero.")
```

> `input()` always returns string. So using int() converts that string to integer. (If possible)

- Operators available:
    - `>`: Greater than
    - `<`: Less than
    - `==`: is equal to
    - `!=`: is not equal to
    - `>=`: Greater than or equal to
    - `<=`: Less than or equal to

- Run this:
```py
x = int(input("Enter a number: "))

match x:
    case 0: # If x is 0
        print("zero")
    case 1: # if x is 1
        print("one")
    case 2: # if x is 2
        print("two")
    case _: # in every other case
        print("I am not ashamed to accept my flaws. I DON'T KNOW THAT NUMBER.")
```
---

## Loop/Iteration

> These statements let you repeatedly execute a block of code.

- Python has:
    - `for loop`: repetition controlled
    - `while loop`: entry condition controlled.
    - Some other language have `do loop` which is exit controlled loop. Python doesn't have those but you can do the same thing using `while(true) loop and break statement`.


- For loop:
```py
for i in range(0,5,1):
    print(i)
```

> This displays numbers 0,1,2,3,4. (**Not 5**).

> `range()` is an iterable in python. i.e. you can loop/iterate through it. It can take upto three values: `range(start,stop,step)`.

- Run this:
```py
for i in range(2,5,1): # You can use different start
    print(i)

for i in range(0,3,1): # Or different stop
    print(i)

for i in range(0,5,2): # Or different step
    print(i)

for i in range(2,11,2): # Or combine
    print(i)

for i in range(0,5): # by default, skip = 1 
    print(i)

for i in range(5): # by default start is 0
    print(i)

for i in range(5,0,-1): # Guess what this displays
    print(i)
```

