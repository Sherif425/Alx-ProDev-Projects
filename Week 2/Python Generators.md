#### **About the Project**

This project introduces advanced usage of Python generators to efficiently handle large datasets, process data in batches, and simulate real-world scenarios involving live updates and memory-efficient computations. The tasks focus on leveraging Python’s `yield` keyword to implement generators that provide iterative access to data, promoting optimal resource utilization, and improving performance in data-driven applications.

#### **Learning Objectives**

By completing this project, you will:

1.  **Master Python Generators**: Learn to create and utilize generators for iterative data processing, enabling memory-efficient operations.
2.  **Handle Large Datasets**: Implement batch processing and lazy loading to work with extensive datasets without overloading memory.
3.  **Simulate Real-world Scenarios**: Develop solutions to simulate live data updates and apply them to streaming contexts.
4.  **Optimize Performance**: Use generators to calculate aggregate functions like averages on large datasets, minimizing memory consumption.
5.  **Apply SQL Knowledge**: Use SQL queries to fetch data dynamically, integrating Python with databases for robust data management.

#### **Requirements**

1.  Proficiency in Python 3.x.
2.  Understanding of `yield` and Python’s generator functions.
3.  Familiarity with SQL and database operations (MySQL and SQLite).
4.  Basic knowledge of database schema design and data seeding.
5.  Ability to use Git and GitHub for version control and submission.

#### 📝 Project Assessment (Hybrid)

Your project will be evaluated primarily through **manual reviews**. To ensure you receive your full score, please:

✅ Complete your project on time  
📄 Submit all required files  
🔗 Generate your review link  
👥 Have your peers review your work

An **auto-check** will also be in place to verify the presence of core files needed for manual review.

##### ⏰ Important Note

If the deadline passes, you won’t be able to generate your review link—so be sure to submit on time!

We’re here to support your learning journey. Happy coding! ✨

##### Quiz questions

**Great!** You've completed the quiz successfully! Keep going! (Show quiz)

##### Question #0

What does the @contextmanager decorator do in Python?

-   It converts a function into an async function
    
-   It provides a shortcut for defining decorators
    
-   It creates a class-based context manager
    
-   It converts a generator function into a context manager
    

---

##### Question #1

Which method is essential for creating a context manager using a class?

-   **new**
    
-   **enter** and **exit**
    
-   **call**
    
-   **del**
    

---

##### Question #2

What is the main difference between Python’s range() in Python 3 and xrange() in Python 2?

-   xrange() is slower than range()
    
-   xrange() is only available in Python 3
    
-   range() returns a generator while xrange() returns a list
    
-   range() returns an immutable sequence, while xrange() returns a generator
    

---

##### Question #3

What is a key advantage of using a generator function over returning a list in Python?

-   Increases execution speed
    
-   Ensures type safety
    
-   Reduces memory usage
    
-   Simplifies code structure
    

---

##### Question #4

What happens if the **exit** method of a context manager returns True after an exception is raised?

-   The program terminates
    
-   The context manager is reset to its initial state
    
-   The exception is re-raised
    
-   The exception is suppressed
    

---

##### Question #5

How can a Python decorator handle functions with different arguments?

-   Use _args and \*_kwargs in the wrapper function
    
-   Modify the original function to match the wrapper signature
    
-   Use a specific argument signature for the wrapper function
    
-   Decorators cannot handle functions with arguments
    

---

##### Question #6

Which of the following best describes a Python decorator?

-   A function that wraps another function to modify its behavior
    
-   A method for optimizing code execution
    
-   A function that replaces another function
    
-   A way to repeat the execution of a function
    

---

##### Question #7

Which statement about generator expressions is true?

-   They always consume more memory than list comprehensions
    
-   They return lists that are lazily evaluated
    
-   They cannot be composed with other generators
    
-   They are syntactically similar to list comprehensions but use parentheses instead of square brackets
    

---

##### Question #8

In an asynchronous Python program, what does asyncio.run() do?

-   Converts a function into a coroutine
    
-   Starts an event loop without blocking
    
-   Runs the given coroutine and blocks until it is complete
    
-   Schedules a coroutine to run later
    

---

##### Question #9

How can you turn a list comprehension into a generator expression?

-   Use double square brackets \[\[ \]\]
    
-   Add a yield statement inside the comprehension
    
-   Use curly braces { } instead of square brackets
    
-   Use parentheses ( ) instead of square brackets
    

## Tasks

##### 0\. Getting started with python generators

mandatory

Score: 65.0% (Checks completed: 100.0%)

**Objective: create a generator that streams rows from an SQL database one by one.**

**Instructions:**

-   Write a python script that `seed.py`:
    
    -   Set up the MySQL database, `ALX_prodev` with the table user\_data with the following fields:
    -   `user_id(Primary Key, UUID, Indexed)`
    -   `name (VARCHAR, NOT NULL)`
    -   `email (VARCHAR, NOT NULL)`
    -   `age (DECIMAL,NOT NULL)`
    -   Populate the database with the sample data from this [user\_data.csv](/rltoken/kPrtJ_hN0TXKgEfwKY4vHg "user_data.csv")
        -   Prototypes:
    -   `def connect_db()` :- connects to the mysql database server
    -   `def create_database(connection)`:- creates the database `ALX_prodev` if it does not exist
    -   `def connect_to_prodev()` connects the the ALX\_prodev database in MYSQL
    -   `def create_table(connection)`:- creates a table user\_data if it does not exists with the required fields
    -   `def insert_data(connection, data)`:- inserts data in the database if it does not exist

```
faithokoth@ubuntu:python-generators-0x00 % cat 0-main.py
#!/usr/bin/python3

seed = __import__('seed')

connection = seed.connect_db()
if connection:
    seed.create_database(connection)
    connection.close()
    print(f"connection successful")

    connection = seed.connect_to_prodev()

    if connection:
        seed.create_table(connection)
        seed.insert_data(connection, 'user_data.csv')
        cursor = connection.cursor()
        cursor.execute(f"SELECT SCHEMA_NAME FROM INFORMATION_SCHEMA.SCHEMATA WHERE SCHEMA_NAME = 'ALX_prodev';")
        result = cursor.fetchone()
        if result:
            print(f"Database ALX_prodev is present ")
        cursor.execute(f"SELECT * FROM user_data LIMIT 5;")
        rows = cursor.fetchall()
        print(rows)
        cursor.close()

faithokoth@ubuntu:python-generators-0x00 % ./0-main.py
connection successful
Table user_data created successfully
Database ALX_prodev is present 
[('00234e50-34eb-4ce2-94ec-26e3fa749796', 'Dan Altenwerth Jr.', 'Molly59@gmail.com', 67), ('006bfede-724d-4cdd-a2a6-59700f40d0da', 'Glenda Wisozk', 'Miriam21@gmail.com', 119), ('006e1f7f-90c2-45ad-8c1d-1275d594cc88', 'Daniel Fahey IV', 'Delia.Lesch11@hotmail.com', 49), ('00af05c9-0a86-419e-8c2d-5fb7e899ae1c', 'Ronnie Bechtelar', 'Sandra19@yahoo.com', 22), ('00cc08cc-62f4-4da1-b8e4-f5d9ef5dbbd4', 'Alma Bechtelar', 'Shelly_Balistreri22@hotmail.com', 102)]

faithokoth@h@ubuntu:python-generators-0x00 % 

```

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `python-generators-0x00`
-   File: `seed.py, README.md`

Check submission View results

##### 1\. generator that streams rows from an SQL database

mandatory

Score: 65.0% (Checks completed: 100.0%)

**Objective:** create a generator that streams rows from an SQL database one by one.

**Instructions:**

-   In `0-stream_users.py` write a function that uses a generator to fetch rows one by one from the `user_data` table. You must use the Yield python generator
    
    -   Prototype: `def stream_users()`
    -   Your function should have no more than 1 loop

```
(venv)faithokoth@Faiths-MacBook-Pro python-generators-0x00 % cat 1-main.py 

#!/usr/bin/python3
from itertools import islice
stream_users = __import__('0-stream_users')

# iterate over the generator function and print only the first 6 rows

for user in islice(stream_users(), 6):
    print(user)

(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00 %./1-main.py

{'user_id': '00234e50-34eb-4ce2-94ec-26e3fa749796', 'name': 'Dan Altenwerth Jr.', 'email': 'Molly59@gmail.com', 'age': 67}
{'user_id': '006bfede-724d-4cdd-a2a6-59700f40d0da', 'name': 'Glenda Wisozk', 'email': 'Miriam21@gmail.com', 'age': 119}
{'user_id': '006e1f7f-90c2-45ad-8c1d-1275d594cc88', 'name': 'Daniel Fahey IV', 'email': 'Delia.Lesch11@hotmail.com', 'age': 49}
{'user_id': '00af05c9-0a86-419e-8c2d-5fb7e899ae1c', 'name': 'Ronnie Bechtelar', 'email': 'Sandra19@yahoo.com', 'age': 22}
{'user_id': '00cc08cc-62f4-4da1-b8e4-f5d9ef5dbbd4', 'name': 'Alma Bechtelar', 'email': 'Shelly_Balistreri22@hotmail.com', 'age': 102}
{'user_id': '01187f09-72be-4924-8a2d-150645dcadad', 'name': 'Jonathon Jones', 'email': 'Jody.Quigley-Ziemann33@yahoo.com', 'age': 116}

(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00 %

```

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `python-generators-0x00`
-   File: `0-stream_users.py`

Check submission View results

##### 2\. Batch processing Large Data

mandatory

Score: 48.75% (Checks completed: 75.0%)

**Objective:** Create a generator to fetch and process data in batches from the users database

**Instructions:**

-   Write a function `stream_users_in_batches(batch_size)` that fetches rows in batches
    
-   Write a function `batch_processing() that processes each batch to filter users over the age of`25\`
    
-   You must use no more than 3 loops in your code. Your script must use the `yield generator`
    
    -   Prototypes:
        
        -   `def stream_users_in_batches(batch_size)`
        -   `def batch_processing(batch_size)`

```
(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00 % cat 2-main.py                
#!/usr/bin/python3
import sys
processing = __import__('1-batch_processing')

##### print processed users in a batch of 50
try:
    processing.batch_processing(50)
except BrokenPipeError:
    sys.stderr.close()

(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00 % ./2-main.py | head -n 5 

{'user_id': '00234e50-34eb-4ce2-94ec-26e3fa749796', 'name': 'Dan Altenwerth Jr.', 'email': 'Molly59@gmail.com', 'age': 67}

{'user_id': '006bfede-724d-4cdd-a2a6-59700f40d0da', 'name': 'Glenda Wisozk', 'email': 'Miriam21@gmail.com', 'age': 119}

{'user_id': '006e1f7f-90c2-45ad-8c1d-1275d594cc88', 'name': 'Daniel Fahey IV', 'email': 'Delia.Lesch11@hotmail.com', 'age': 49}

{'user_id': '00cc08cc-62f4-4da1-b8e4-f5d9ef5dbbd4', 'name': 'Alma Bechtelar', 'email': 'Shelly_Balistreri22@hotmail.com', 'age': 102}

{'user_id': '01187f09-72be-4924-8a2d-150645dcadad', 'name': 'Jonathon Jones', 'email': 'Jody.Quigley-Ziemann33@yahoo.com', 'age': 116}

(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00 % 

```

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `python-generators-0x00`
-   File: `1-batch_processing.py`

Check submission View results

##### 3\. Lazy loading Paginated Data

mandatory

Score: 43.33% (Checks completed: 66.67%)

**Objective:** Simulte fetching paginated data from the users database using a generator to lazily load each page

**Instructions:**

-   Implement a generator function lazy_paginate(page_size) that implements the `paginate_users(page_size, offset)` that will only fetch the next page when needed at an offset of `0`.
    
    -   You must only use one `loop`
    -   Include the `paginate_users` function in your code
    -   You must use the `yield` generator
    -   Prototype:
    -   `def lazy_paginate(page_size)`

```
#!/usr/bin/python3
seed = __import__('seed')


def paginate_users(page_size, offset):
    connection = seed.connect_to_prodev()
    cursor = connection.cursor(dictionary=True)
    cursor.execute(f"SELECT * FROM user_data LIMIT {page_size} OFFSET {offset}")
    rows = cursor.fetchall()
    connection.close()
    return rows




(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00 % cat 3-main.py
#!/usr/bin/python3
import sys
lazy_paginator = __import__('2-lazy_paginate').lazy_pagination


try:
    for page in lazy_paginator(100):
        for user in page:
            print(user)

except BrokenPipeError:
    sys.stderr.close()
(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00  % python 3-main.py | head -n 7

{'user_id': '00234e50-34eb-4ce2-94ec-26e3fa749796', 'name': 'Dan Altenwerth Jr.', 'email': 'Molly59@gmail.com', 'age': 67}

{'user_id': '006bfede-724d-4cdd-a2a6-59700f40d0da', 'name': 'Glenda Wisozk', 'email': 'Miriam21@gmail.com', 'age': 119}

{'user_id': '006e1f7f-90c2-45ad-8c1d-1275d594cc88', 'name': 'Daniel Fahey IV', 'email': 'Delia.Lesch11@hotmail.com', 'age': 49}

{'user_id': '00af05c9-0a86-419e-8c2d-5fb7e899ae1c', 'name': 'Ronnie Bechtelar', 'email': 'Sandra19@yahoo.com', 'age': 22}

{'user_id': '00cc08cc-62f4-4da1-b8e4-f5d9ef5dbbd4', 'name': 'Alma Bechtelar', 'email': 'Shelly_Balistreri22@hotmail.com', 'age': 102}

{'user_id': '01187f09-72be-4924-8a2d-150645dcadad', 'name': 'Jonathon Jones', 'email': 'Jody.Quigley-Ziemann33@yahoo.com', 'age': 116}

{'user_id': '01ab6c5d-7ae2-4968-991a-d63e93d8d025', 'name': 'Forrest Heaney', 'email': 'Albert51@hotmail.com', 'age': 104}
(venv) faithokoth@Faiths-MacBook-Pro python-generators-0x00 % 
```

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `python-generators-0x00`
-   File: `2-lazy_paginate.py`

Check submission View results

##### 4\. Memory-Efficient Aggregation with Generators

mandatory

Score: 32.5% (Checks completed: 50.0%)

**Objective:** to use a generator to compute a memory-efficient aggregate function i.e average age for a large dataset

**Instruction:**

-   Implement a generator `stream_user_ages()` that yields user ages one by one.
    
-   Use the generator in a different function to calculate the average age without loading the entire dataset into memory
    
-   Your script should print `Average age of users: average age`
    
-   You must use no more than two loops in your script
    
-   You are not allowed to use the SQL `AVERAGE`
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `python-generators-0x00`
-   File: `4-stream_ages.py`

Check submission View results

##### 5\. Manual Review

mandatory

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `python-generators-0x00`

