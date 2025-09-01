# Project: Advanced shell scripting | Cairo Intranet

ProDev Backend Average: 83.34%

-   [
    
    Back-End Web Development Average: 96.1%
    
    
    
    ](/curriculums/70/observe)
-   [
    
    ProDev Backend Average: 83.34%
    
    
    
    ](/curriculums/86/observe)
-   [
    
    Professional Foundations Average: 94.18%
    
    
    
    ](/curriculums/89/observe)

Week 7

Week 7

-   [Week 0](/projects/102638)
-   [Week 1](/concepts/113077?project_id=102975)
-   [Week 2](/projects/101641)
-   [Week 3](/projects/102758)
-   [Week 4](/projects/101642)
-   [Week 5](/projects/101622)
-   [Week 6](/projects/209)
-   [Week 7](/projects/102965)
-   [Week 8](/projects/102087)
-   [Week 9](/projects/101632)
-   [Week 10](/projects/102428)
-   [Week 11](/projects/102426)

## Advanced shell scripting

[

Advanced Shell Scripting: Automating Tasks and Managing Processes

](/concepts/108709?project_id=101627)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101627)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101627)[

Advanced shell scripting

](/projects/101627)

## Git-Flows

[

Version Control: Advanced Git Techniques and Workflows.

](/concepts/108710?project_id=101629)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101629)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101629)[

Git-Flows

](/projects/101629)

## Containerization with docker

[

Containerization: Introduction to Docker and Container Orchestration with Kubernetes

](/concepts/107383?project_id=101630)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101630)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101630)[

Containerization with docker

](/projects/101630)

## Web Infrastructure

[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=302)[

DNS

](/concepts/12?project_id=302)[

Monitoring

](/concepts/13?project_id=302)[

Web Server

](/concepts/17?project_id=302)[

Network basics

](/concepts/33?project_id=302)[

Load balancer

](/concepts/46?project_id=302)[

Server

](/concepts/67?project_id=302)[

0x09. Web infrastructure design

](/projects/302)

## Work Log (Month 2)

[

What Is a Work Log and Why Bother? (a.k.a. Your Brag List)

](/concepts/111671?project_id=102965)[

How to Keep and Update Your Work Log

](/concepts/111674?project_id=102965)[

Update Your Monthly Work Log (Month 2) — ProDev Back-end

](/projects/102965)

# Advanced shell scripting

-   Novice
-   Weight: 1
-   Project over - took place from Aug 4, 2025 1:00 AM to Aug 11, 2025 1:00 AM
-   Manual QA review was done on Aug 9, 2025 2:45 AM
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Manual QA review:** 6.0/6 mandatory
-   **Auto QA review:** 18.0/22 mandatory
-   **Altogether:**  **85.71%**
    -   Mandatory: 85.71%
    -   Optional: no optional tasks

**Overall comment:**

Good Job

### Project Overview & Summary

This project is a practical deep dive into Advanced Shell Scripting, focusing on automating interactions with a RESTful API (the Pokémon API). It progresses from simple, single API calls to complex operations involving parallel processing, robust error handling, and data summarization. The goal is to simulate real-world DevOps and Data Engineering tasks where automation, reliability, and efficiency are paramount.

#### **Learning Objectives**

By completing this project, you will learn and demonstrate proficiency in:

1.  **API Interaction:** Making HTTP requests from the command line using `curl`.
2.  **JSON Manipulation:** Parsing, filtering, and extracting data from JSON responses using `jq`.
3.  **Text Processing:** Utilizing the UNIX text processing trifecta (`grep`, `sed`, `awk`) to transform and format data.
4.  **Robust Scripting:** Implementing error handling, status checking, and retry logic to create reliable automation scripts.
5.  **Process Management:** Using shell job control (`&`, `wait`, `$!`) to run tasks in parallel, significantly improving script performance.
6.  **Data Reporting:** Aggregating data from multiple sources and generating structured reports (e.g., CSV files).
7.  **Modular Design:** Structuring scripts to be maintainable and adaptable for future changes.

#### **Key Concepts**

-   **HTTP Status Codes:** Checking `curl` exit codes or HTTP status codes (e.g., `200` OK vs. `404` Not Found) to determine the success or failure of a request.
-   **Idempotency and Retries:** Designing operations to be safely retried in case of transient network failures.
-   **Rate Limiting:** Understanding the constraints of external APIs and implementing delays to avoid being blocked.
-   **Concurrency vs. Parallelism:** Using background processes to achieve parallelism in a shell environment, understanding the associated challenges (e.g., shared resources, output interleaving).
-   **Data Pipelines:** Building a complete pipeline: data extraction (API) -> transformation (parsing) -> loading (saving to files) -> reporting (summary/analytics).

#### **Tools and Libraries**

-   **`curl`:** The primary tool for transferring data from or to a server. Used to make GET requests to the Pokémon API.
-   **`jq`:** A lightweight and powerful command-line JSON processor. Essential for parsing the API response and extracting specific fields.
-   **`awk`:** A versatile programming language for pattern scanning and processing. Used for text extraction, report generation, and calculating averages.
-   **`sed`:** A stream editor for filtering and transforming text. Used for specific text substitutions.
-   **Core Shell Utilities:** `grep`, `cut`, `echo`, variables, loops, conditionals, functions, and process control (`&&`, `||`).

#### **Real-World Use Case**

This project mirrors a common pattern in cloud and data engineering:

A **Data Engineer** needs to build a pipeline to collect data from various external SaaS platforms (e.g., Salesforce, Shopify, Twitter API) on a daily basis. 1. **Extraction:** The scripts from **Tasks 0, 2, 4, and 5** represent the data extraction layer. They must be robust, handle API failures gracefully, and efficiently pull data from all required endpoints. 2. **Transformation:** The scripts from **Tasks 1 and 3** represent the transformation layer. Raw JSON data is parsed, cleaned, and formatted into a more usable structure (like a CSV) for analysts. 3. **Loading:** The final JSON and CSV files are the loaded data, ready to be consumed by a database or a Business Intelligence (BI) tool like Tableau or Power BI.

The skills practiced here are directly applicable to building ETL (Extract, Transform, Load) or ELT pipelines using shell scripts, which is a lightweight and powerful approach for many tasks.

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

What is a key disadvantage of shell scripts?

-   Easy debugging
    
-   Well-suited for large and complex tasks
    
-   High execution speed
    
-   Prone to costly errors
    

---

##### Question #1

What is the purpose of the .bashrc file?

-   To execute commands and scripts at every terminal session start
    
-   To manage file permissions
    
-   To store kernel configuration settings
    
-   To provide a graphical user interface
    

---

##### Question #2

What does the grep command do in Linux?

-   Searches for a pattern in a file and prints matching lines
    
-   Compiles code into a binary executable
    
-   Prints the contents of a file
    
-   Edits a file by replacing text
    

---

##### Question #3

What is the primary function of a Linux shell?

-   Providing a graphical user interface (GUI)
    
-   Compiling code into machine language
    
-   Managing system hardware
    
-   Interpreting and executing user commands
    

---

##### Question #4

In awk, what does $1 represent?

-   The last field in a line
    
-   The number of fields in a line
    
-   The first field in a line
    
-   The entire line
    

---

##### Question #5

Which key combination is used to send the SIGINT signal to a running process in the foreground?

-   CTRL + C
    
-   CTRL + Q
    
-   CTRL + Z
    
-   CTRL + D
    

---

##### Question #6

Which grep option is used to ignore case sensitivity during a search?

-   \-c
    
-   \-i
    
-   \-v
    
-   \-l
    

---

##### Question #7

What does the bg command do in Bash?

-   Moves a background process to the foreground
    
-   Resumes a stopped process in the background
    
-   Stops a running process
    
-   Suspends a running process
    

---

##### Question #8

Which command would you use to replace all occurrences of “input” with “output” in a file using `sed`?

-   sed ‘s/input/output/’
    
-   sed ‘g/input/output/’
    
-   sed ‘r/input/output/’
    
-   sed ‘f/input/output/’
    

---

##### Question #9

Which of the following commands would you use to list all files in a directory in a long listing format?

-   ls -l
    
-   pwd -l
    
-   ls -a
    
-   cat -l
    

## Tasks

##### 0\. API Request Automation

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Automate the process of making API requests to the Pokémon API and saving the results to a file

**Instructions:**

-   Write a shell script that makes a request to the [Pokémon API](/rltoken/jqW_W_52FxzA4GyiMpNQSw "Pokémon API") and retrieves data for a specific Pokémon Pikachu.
    
-   It should save the response to a json file: data.json
    
-   If the request fails, it should log the error to an error file: errors.txt
    

**Sample Output**

```
ghostmode@GhostMode:~$ jq . < data.json | head -n 50
{
  "abilities": [
    {
      "ability": {
        "name": "static",
        "url": "https://pokeapi.co/api/v2/ability/9/"
      },
      "is_hidden": false,
      "slot": 1
    },
    {
      "ability": {
        "name": "lightning-rod",
        "url": "https://pokeapi.co/api/v2/ability/31/"
      },
      "is_hidden": true,
      "slot": 3
    }
  ],
  "base_experience": 112,
  "cries": {
    "latest": "https://raw.githubusercontent.com/PokeAPI/cries/main/cries/pokemon/latest/25.ogg",
    "legacy": "https://raw.githubusercontent.com/PokeAPI/cries/main/cries/pokemon/legacy/25.ogg"
  },
  "forms": [
    {
      "name": "pikachu",
      "url": "https://pokeapi.co/api/v2/pokemon-form/25/"
    }
  ],
  "game_indices": [
    {
      "game_index": 84,
      "version": {
        "name": "red",
        "url": "https://pokeapi.co/api/v2/version/1/"
      }
    },
    {
      "game_index": 84,
      "version": {
        "name": "blue",
        "url": "https://pokeapi.co/api/v2/version/2/"
      }
    },
    {
      "game_index": 84,
      "version": {
        "name": "yellow",
        "url": "https://pokeapi.co/api/v2/version/3/"
ghostmode@GhostMode:~$
```

**Repo:**

-   GitHub repository: `ALXprodev-Devops`
-   Directory: `Advanced_shell`
-   File: `apiAutomation-0x00`

Check submission View results

##### 1\. Extract Pokémon Data

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Use advanced text manipulation tools (jq, awk, sed) to extract specific data from the API response.

**Instructions:**

-   Write a script that extracts the Pokémon’s name, height, weight, and type from the JSON file created in Task 0.
    
-   Format the output in a human-readable way,`“Pikachu is of type Electric, weighs 6kg, and is 0.4m tall.”`
    
-   You should only use these commands: jq, awk, sed
    

**Sample Output:**

```
ghostmode@GhostMode:~$ ./parse_pikachu
Pikachu is of type Electric, weighs 6kg, and is 0.4m tall.
ghostmode@GhostMode:~$
```

**Repo:**

-   GitHub repository: `ALXprodev-Devops`
-   Directory: `Advanced_shell`
-   File: `data_extraction_automation-0x01`

Check submission View results

##### 2\. Batch Pokémon Data Retrieval

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Automate the retrieval of data for multiple Pokémon and store it in separate files.

**Instructions:**

-   Create a script that loops through a list of Pokémon \[Bulbasaur, Ivysaur, Venusaur, Charmander, Charmeleon\]
    
-   For each Pokémon, retrieve its data from the API and save it to a separate file named after the Pokémon (e.g., pikachu.json, bulbasaur.json…).
    
-   Handle any potential rate-limiting issues by adding a delay between requests.
    

**Sample Output:**

```
ghostmode@GhostMode:~$ ./fetch_multiple_pokemon
Fetching data for bulbasaur...
Saved data to pokemon_data/bulbasaur.json ✅
Fetching data for ivysaur...
Saved data to pokemon_data/ivysaur.json ✅
Fetching data for venusaur...
Saved data to pokemon_data/venusaur.json ✅
Fetching data for charmander...
Saved data to pokemon_data/charmander.json ✅
Fetching data for charmeleon...
Saved data to pokemon_data/charmeleon.json ✅
ghostmode@GhostMode:~$ jq . < pokemon_data/bulbasaur.json | head -n 30
{
  "abilities": [
    {
      "ability": {
        "name": "overgrow",
        "url": "https://pokeapi.co/api/v2/ability/65/"
      },
      "is_hidden": false,
      "slot": 1
    },
    {
      "ability": {
        "name": "chlorophyll",
        "url": "https://pokeapi.co/api/v2/ability/34/"
      },
      "is_hidden": true,
      "slot": 3
    }
  ],
  "base_experience": 64,
  "cries": {
    "latest": "https://raw.githubusercontent.com/PokeAPI/cries/main/cries/pokemon/latest/1.ogg",
    "legacy": "https://raw.githubusercontent.com/PokeAPI/cries/main/cries/pokemon/legacy/1.ogg"
  },
  "forms": [
    {
      "name": "bulbasaur",
      "url": "https://pokeapi.co/api/v2/pokemon-form/1/"
    }
  ],
ghostmode@GhostMode:~$
```

**Repo:**

-   GitHub repository: `ALXprodev-Devops`
-   Directory: `Advanced_shell`
-   File: `batchProcessing-0x02`

Check submission View results

##### 3\. Summarize Pokémon Data

mandatory

Score: 25.0% (Checks completed: 25.0%)

**Objective:** Create a report that summarizes data for multiple Pokémon.

**Instructions:**

-   Write a shell script that reads all the JSON files generated in Task 2 and extracts the name, height, and weight of each Pokémon.
    
-   Generate a CSV file containing the Pokémon’s name, height, and weight.
    
-   Use awk to calculate the average height and weight of all Pokémon in the report.
    

**Sample Output:**

```
ghostmode@GhostMode:~$ ./pokemon_report
CSV Report generated at: pokemon_report.csv

Name,Height (m),Weight (kg)
Bulbasaur,0.7,6.9
Charmander,0.6,8.5
Charmeleon,1.1,19.0
Ivysaur,1.0,13.0
Venusaur,2.0,100.0

Average Height: 1.08 m
Average Weight: 29.48 kg
ghostmode@GhostMode:~$
```

**Repo:**

-   GitHub repository: `ALXprodev-Devops`
-   Directory: `Advanced_shell`
-   File: `summaryData-0x03`

Check submission Mark submission : in progress... : an error occurred View results

##### 4\. Error Handling and Retry Logic

mandatory

Score: 66.67% (Checks completed: 66.67%)

**Objective:** Add robust error handling and retry logic for API requests.

**Instructions:**

-   Modify the script from Task 2 to handle potential errors (e.g., network issues, invalid Pokémon names).
    
-   If an API request fails, implement a retry mechanism that attempts the request up to 3 times before logging the error and skipping to the next Pokémon.
    

**Repo:**

-   GitHub repository: `ALXprodev-Devops`
-   Directory: `Advanced_shell`
-   File: `batchProcessing-0x02`

Check submission Mark submission : in progress... : an error occurred View results

##### 5\. Parallel Data Fetching

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Speed up data retrieval using parallel processing.

**Instructions:**

-   Write a script that fetches data for these `Pokémon[Bulbasaur, Ivysaur, Venusaur, Charmander, Charmeleon ]` in parallel by leveraging background processes and process management tools.
    
-   Ensure that the script handles background processes properly and waits for all processes to complete before moving to the next step.
    

**Repo:**

-   GitHub repository: `ALXprodev-Devops`
-   Directory: `Advanced_shell`
-   File: `batchProcessing-0x04`

Check submission View results

##### 6\. Manual Review

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Repo:**

-   GitHub repository: `ALXprodev-Devops`
-   Directory: `Advanced_shell`

View results

Ready for a new review

[

Back

](/concepts/111449?project_id=101627)

[

Next

](/concepts/108710?project_id=101629)

Copyright © 2025 ALX, All rights reserved.