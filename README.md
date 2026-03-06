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
| chart-type     | Topic or sub-topic of the question              |
| page_number    | Page number from which the question was scraped |
| question       | The aptitude question text                      |
| option_a       | First answer option                             |
| option_b       | Second answer option                            |
| option_c       | Third answer option                             |
| option_d       | Fourth answer option                            |
| correct_answer | The correct option for the question             |
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

