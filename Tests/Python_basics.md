## Question: Object-Oriented Programming (27 marks)

You are required to design a simple library management system using Object-Oriented Programming (OOP) principles. The system should be able to manage books and members. Each book has a title, author, and ISBN number. Each member has a name, membership ID, and a list of borrowed books.

### Class Descriptions:

#### Book Class
| Attribute/Method | Description |
|------------------|-------------|
| `title`          | `str`: The title of the book |
| `author`         | `str`: The author of the book |
| `isbn`           | `str`: The ISBN number of the book |
| `get_title()`    | Returns the title of the book |
| `set_title(title)` | Sets the title of the book |
| `get_author()`   | Returns the author of the book |
| `set_author(author)` | Sets the author of the book |
| `get_isbn()`     | Returns the ISBN number of the book |
| `set_isbn(isbn)` | Sets the ISBN number of the book |

#### Member Class
| Attribute/Method | Description |
|------------------|-------------|
| `name`           | `str`: The name of the member |
| `membership_id`  | `str`: The membership ID of the member |
| `borrowed_books` | `list`: A list of books borrowed by the member |
| `get_name()`     | Returns the name of the member |
| `set_name(name)` | Sets the name of the member |
| `get_membership_id()` | Returns the membership ID of the member |
| `set_membership_id(membership_id)` | Sets the membership ID of the member |
| `borrow_book(book)` | Adds a book to the member's list of borrowed books |
| `return_book(book)` | Removes a book from the member's list of borrowed books |

### Tasks:

1. **Declare the `Book` Class (5 marks)**
   - Write program code to declare the `Book` class, its attributes, and constructor.
   - Do not write program code for the get methods.
   - Use your programming language's appropriate constructor.
   - All attributes must be private. If you are writing in Python, include attribute declarations using comments.
   - Save your program as `Question1_N22`.
   - Copy and paste the program code into part 1(a) in the evidence document.

2. **Define `Book` Class Methods (6 marks)**
   - Write program code for the class methods `get_title()`, `set_title(title)`, `get_author()`, `set_author(author)`, `get_isbn()`, and `set_isbn(isbn)`.
   - Save your program.
   - Copy and paste the program code into part 1(b) in the evidence document.

3. **Declare the `Member` Class (5 marks)**
   - Write program code to declare the `Member` class, its attributes, and constructor.
   - Do not write program code for the get methods.
   - Use your programming language's appropriate constructor.
   - All attributes must be private. If you are writing in Python, include attribute declarations using comments.
   - Save your program as `Question1_N22`.
   - Copy and paste the program code into part 1(c) in the evidence document.

4. **Define `Member` Class Methods (6 marks)**
   - Write program code for the class methods `get_name()`, `set_name(name)`, `get_membership_id()`, `set_membership_id(membership_id)`, `borrow_book(book)`, and `return_book(book)`.
   - Save your program.
   - Copy and paste the program code into part 1(d) in the evidence document.

5. **Main Program (5 marks)**
   - Write a main program to demonstrate the use of these classes and methods.
   - The program should create instances of `Book` and `Member`, and demonstrate borrowing and returning books.
   - Save your program.
   - Copy and paste the program code into part 1(e) in the evidence document.

## Question: File Handling (20 marks)

You are required to write a Python program that reads from a text file containing student names and their scores in various subjects, processes the data, and writes the results to another text file. The input file `students.csv` should have the following format:

### Tasks:

1. **Create the CSV File (3 marks)**
   - Write program code to create a text file `students.csv` with the given header and data.
   - Save your program as `Question2_N22`.
   - Copy and paste the program code into part 2(a) in the evidence document.
```
Name, English, Computer, Maths, Physics
John Doe, 85, 90, 78, 92
Jane Smith, 88, 85, 91, 89
Alice Johnson, 79, 92, 84, 87
Bob Brown, 90, 88, 85, 91
Charlie Davis, 82, 87, 89, 85
```
2. **Read Data from File (5 marks)**
   - Write a Python function `read_file()` to read the data from `students.csv` and store it in a 2D array.
   - Use appropriate exception handling to manage file reading errors.
   - Save your program.
   - Copy and paste the program code into part 2(b) in the evidence document.

3. **Calculate and Display Averages and Percentages (6 marks)**
   - Using the array from part 2, write a Python function `calculate_averages()` to calculate and display the average score and percentage for each student.
   - The percentage should be calculated as the average of the scores in all subjects.
   - Save your program.
   - Copy and paste the program code into part 2(c) in the evidence document.

4. **Write Results to New File (6 marks)**
   - Write a Python function `write_results()` to create a new file `results.csv` and add the calculated averages and percentages for each student.
   - The new file should have the following format:
     ```
     Name, English, Computer, Maths, Physics, Average, Percentage
     John Doe, 85, 90, 78, 92, 86.25, 86.25%
     Jane Smith, 88, 85, 91, 89, 88.25, 88.25%
     Alice Johnson, 79, 92, 84, 87, 85.5, 85.5%
     Bob Brown, 90, 88, 85, 91, 88.5, 88.5%
     Charlie Davis, 82, 87, 89, 85, 85.75, 85.75%
     ```
   - Save your program.
   - Copy and paste the program code into part 2(d) in the evidence document.

5. **Main Program (5 marks)**
   - Write a main program to demonstrate the use of these functions.
   - The program should create the `students.csv` file, read the data, calculate the averages and percentages, and write the results to `results.csv`.
   - Save your program.
   - Copy and paste the program code into part 2(e) in the evidence document.