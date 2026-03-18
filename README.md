# IndiaBIX DataInterpretation Scraper
## Overview
This project is a Python-based web scraping tool that collects datainterpretation multiple-choice questions from the IndiaBIX website and stores them in a structured CSV dataset. The scraper navigates through different topics and paginated pages to extract questions, answer options, and the correct answers.
The goal of this project is to build a structured dataset that can be used for learning purposes, data analysis, or machine learning applications .
## Features
* Automatically navigates through multiple datainterpretation topics.
* Handles paginated question pages.
* Extracts question text and four answer options.
* Detects the correct answer by interacting with the webpage.
* Saves the collected data in a structured CSV file.
* Implements basic validation to avoid missing or incomplete records.
* Includes delays to simulate human browsing behavior.

## Dataset Information

The generated dataset is stored in a CSV file containing the following columns:

| Column Name    | Description                                     |
| -------------- | ----------------------------------------------- |
| Section        | Which module it belongs to              |
| TopicName      | Topic or sub-topic of the question              |
| PageNumber     | Page number from which the question was scraped |
| ImageURL       | Images of particular chart type                 |
| Question       | The aptitude question text                      |
| Option_A       | First answer option                             |
| Option_B       | Second answer option                            |
| Option_C       | Third answer option                             |
| Option_D       | Fourth answer option                            |
| CorrectAnswer | The correct option for the question             |
## Technologies Used
* **Python** – Core programming language
* **Selenium WebDriver** – Browser automation for scraping dynamic content
* **ChromeDriver** – WebDriver used for controlling Google Chrome
* **CSV Module** – Used to store scraped data in a structured format
## How the Scraper Works
1. The script first opens the IndiaBIX aptitude index page.
2. It automatically collects all available aptitude topics.
3. For each topic, it identifies sub-sections such as:
   *Table Charts-1
   *Bar Charts-1
   *Pie Charts-1
   *Line Charts-1
5. The scraper navigates through paginated question pages.
6. For every question block, it extracts:
   * Question text
   * Four options
   * Correct answer
7. The extracted data is written into the CSV file.
## Limitations
* The scraper depends on the structure of the website. If the website layout changes, the script may need updates.
* Execution time may be longer due to pagination and built-in delays.
* The scraper currently focuses on aptitude questions only.
## Future Improvements
* Export dataset to additional formats such as JSON or Excel.
* Implement logging for better monitoring.
* Add automated duplicate detection.
* Build a dataset preprocessing pipeline for machine learning applications.
# IndiaBix Aptitude Scraper
## Overview
This project is a Python-based web scraper that collects aptitude questions from the IndiaBix website.
It uses **Selenium WebDriver** to automate the browser and extract questions, options, and correct answers from different aptitude topics.
The scraped data is stored in a **CSV file** for easy analysis and practice.
## Features
* Scrapes aptitude questions from IndiaBix
* Extracts:
  * Question
  * Options (A, B, C, D)
  * Correct Answer
* Handles pagination automatically
* Stores data in CSV format
* Includes delays to mimic human browsing and avoid blocking
## Technologies Used
* Python
* Selenium
* CSV
* Chrome WebDriver
## Data Representation
The scraped data is stored in a **CSV file** with the following columns:
| Column Name    | Description                                     |
| -------------- | ----------------------------------------------- |
| Section        | Which module it belongs to                      |
| TopicName      | Topic or sub-topic of the question              |
| PageNumber     | Page number from which the question was scraped |
| ImageURL       |If image present store url or store null         |
| Question       | The aptitude question text                      |
| Option_A       | First answer option                             |
| Option_B       | Second answer option                            |
| Option_C       | Third answer option                             |
| Option_D       | Fourth answer option                            |
| CorrectAnswer | The correct option for the question             |
## Future Improvements
*Extend the scraper to collect data from all aptitude categories and topics available on the website.
*Add support for exporting data in multiple formats such as Excel and JSON.
*Implement error handling and logging to track scraping progress and failures.
*Store the scraped data in a database like MySQL or SQLite instead of only CSV.
## IndiaBix Data Interpretation Scraper with MySQL Storage
## Description
This project is a web scraping tool built using Python and Selenium to extract Data Interpretation questions, options, answers, and explanations from the IndiaBix website. The scraped data is stored directly into a MySQL database without using intermediate CSV files.
## Features
Automated web scraping using Selenium
Extracts questions, options, correct answers, and explanations
Stores data directly into MySQL database
Configurable base URL for different topics
Structured and clean data storage
## Technologies Used
Python
Selenium
MySQL
SQLAlchemy 
## Requirements
Make sure you have the following installed:
Python 3.x
Google Chrome browser
ChromeDriver (compatible with your Chrome version)
MySQL Server
## Installation
Clone the repository:
git clone <your-repo-link>
cd <project-folder>
Install required Python packages:
pip install selenium mysql-connector-python sqlalchemy
Download and set up ChromeDriver:
Place ChromeDriver in your project folder or system PATH
## Configuration
Update the following in your script:
BASE_URL → Target IndiaBix topic URL
## MySQL credentials:
host="localhost"
user="root"
password="your_password"
database="your_database"
## Usage
Run the script:
python your_script_name.py
The scraper will:
## Open the website
Extract data page by page
Store it directly into the MySQL database
Database Structure
## Example table fields:
id
question
option_a
option_b
option_c
option_d
answer
explanation
