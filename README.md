# AdvancedSoftwareEngineer
# Project's Site
**https://sites.google.com/view/spaceteam2023/home**
# Overview
This project aims to do a research about GitHub.
Research Question: 
Is there a significant difference in the diagram sizes distribution (column count + table count) among different primary coding languages in GitHub repositories?

# Properties
We have 2 main properties in order to answer the research question.
Diagram Size (column count + table count)
Main coding language.
The first property shows the size of the database diagram for the project.
The second property reflects the main coding language used for the project.
The idea is to check the correlation between these 2 variables, which means to see if the distribution of the diagram sizes differs in different coding languages.


# Tools & Technologies

**QuickDatabase Diagram:** QuickDatabaseDiagram is a web  tool used for building a diagram using specific syntax, or getting a sql file as input. This tool takes these variables and converts them into a database diagram that shows all the values included.
(https://www.quickdatabasediagrams.com)

**Selenium:** Selenium is a web automation tool, this tool is used to automate the process of doing a good number of projects, since the process is based on web (GitHub repositories, files, and QuickDatabaseDiagram). This tool is a python package that reads commands and does them in a web browser.

**GitHub API:** GitHub API is used as a way to search for projects instead of going into the website itself and search manually. GitHub API was used to get projects with specific values that are relevant to the project.

**Python:** Since QuickDatabaseDiagram gets a specific syntax as input, We Wrote a code that converts DBML Syntax into QuickDatabaseDiagram syntax.
The output of QuickDatabaseDiagram in PDF, PDF included the tables and their values, a python package was used to read this PDF and count the number of tables & columns.

**matplotlib.pyplot/seaborn:** Used for visualization in the last step to see the results.

**CSV:** the output of running the python code was processed into a CSV that contains all relevant project URLs.

# Work Process

**1. Data Collection:**
Collect a list of GitHub repositories that host DBML files that includes the schema of the project. 
For each repository, retrieve data on the primary coding language, link to DBML file, link to the repository.
Tool used : GitHub API.
<img width="1350" alt="Screenshot 2023-08-20 at 18 31 35" src="https://github.com/HabebNawatha/AdvancedSoftwareEngineer/assets/109216430/5dc03798-d8cc-48e4-b97e-873dfb7e2fbf">


**2. Data Preprocessing:**
Clean the collected data, handling missing values and outliers if necessary.
Filter out repositories with incomplete or insufficient data.
Ensure the data is in a structured format, such as a DataFrame.

**3. Converting Syntax of DBML File:**
Go to the link of the DBML file, read the syntax, convert it to QuickDatabaseDiagram input syntax.
Tool used: Selenium (Web Automation) / Python Code.

**4. QuickDatabaseDiagram Process:**
Go to Quick DatabaseDiagram.
Put the converted syntax as input.
Wait for the tool to show a Diagram.
Export as PDF.
Tool used: Selenium (Web Automation) / QuickDatabaseDiagram.
<img width="808" alt="Screenshot 2023-08-20 at 18 34 52" src="https://github.com/HabebNawatha/AdvancedSoftwareEngineer/assets/109216430/16b9beda-5314-4503-bf83-b8cb4c724322">

**5. Gathering Information About Diagram Size:**
Getting the exported PDF.
Counting columns and tables.
Saving number to the Dataframe.
Tools Used: Python Library (pdfplumber).
<img width="1403" alt="Screenshot 2023-08-20 at 18 37 44" src="https://github.com/HabebNawatha/AdvancedSoftwareEngineer/assets/109216430/bf7a411d-150d-482e-8401-d6c34dc291f2">

**6. Data Preprocess (Second time):**
Clean the collected data, handling missing values and outliers if necessary.
Filter out repositories with incomplete or insufficient data.
Ensure the data is in a structured format, such as a DataFrame.
Delete Null values as in projects that did not work to run.
Normalization.
Tool Used: Python Code (Pandas).

**6. Visualization**
After gathering all the information we built a plot to show our results.
Tool used: matplotlib.pyplot/seaborn.
<img width="1187" alt="Screenshot 2023-12-19 at 20 27 31" src="https://github.com/HabebNawatha/AdvancedSoftwareEngineer/assets/109216430/3a9ebc2e-f661-4a28-b414-93bd040fa22c">


@ All Rights Reserved | University of Haifa
