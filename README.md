# Python-For-Devops
Python

1. Core Concepts

Variables and Data Types:
Store data using variables (e.g., name = "Alice").
Common data types: integers (int), floats (float), strings (str), booleans (bool), lists, tuples, dictionaries, sets.

Control Flow:
Conditional statements: if, elif, else to execute code based on conditions.
Loops: for and while to repeat blocks of code.
Functions:
Reusable blocks of code that perform specific tasks.
Define functions using def keyword.

2. Essential Libraries

os: Interact with the operating system (e.g., file operations, directory navigation).

Python

import os

# Create a directory
os.mkdir("new_directory") 

# Get current working directory
current_dir = os.getcwd() 
sys: Interact with the Python interpreter (e.g., command-line arguments).

Python

import sys

# Access command-line arguments
arguments = sys.argv 
time: Work with time-related operations (e.g., sleep, timestamps).

Python

import time

# Pause execution for 5 seconds
time.sleep(5) 
datetime: Handle dates and times effectively.

Python

from datetime import datetime

# Get current date and time
now = datetime.now() 
3. Automation Examples

File Renaming:

Python

import os

for filename in os.listdir("."):
    if filename.endswith(".txt"):
        new_name = filename.replace(".txt", ".doc")
        os.rename(filename, new_name)
Web Scraping (with requests and Beautiful Soup)

Python

import requests
from bs4 import BeautifulSoup

url = "https://www.example.com"
response = requests.get(url)
soup = BeautifulSoup(response.content, "html.parser")

# Extract data from HTML (e.g., titles, links)
titles = soup.find_all("h1") 
for title in titles:
    print(title.text)
Automating Emails (with smtplib)

Python

import smtplib
from email.mime.text import MIMEText

sender_email = "your_email@example.com"
receiver_email = "recipient_email@example.com"
password = "your_email_password" 

message = MIMEText("This is an automated email.")

with smtplib.SMTP('smtp.gmail.com', 587) as server:
    server.starttls()
    server.login(sender_email, password)
    server.sendmail(sender_email, receiver_email, message.as_string())
4. Key Considerations

Error Handling: Use try-except blocks to gracefully handle potential issues.
Modularity: Break down complex tasks into smaller functions for better organization.
Testing: Write unit tests to ensure your scripts work as expected.
Documentation: Add comments to your code to explain its purpose and functionality.
5. Advanced Topics

GUI Automation (with Selenium)
API Automation (with requests)
Task Scheduling (with schedule or APScheduler)
**Cloud Integration (with AWS, Azure, or GCP) **

