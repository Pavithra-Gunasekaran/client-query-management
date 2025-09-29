📂 Client Query Management System

🚀 Project Overview

This is a full-stack Python web application built using Streamlit and MySQL to manage customer support queries. It provides separate secure interfaces for Clients (to submit queries) and Support Staff (to view, filter, and close queries).


💻 Key Features

User Authentication: Secure login and registration with two distinct roles:

Client: Can submit new queries.

Support: Can view, filter, and close all submitted queries.

Query Submission: A dedicated Streamlit form for clients to submit new queries, capturing details like email, mobile, heading, and description.

Support Dashboard: An interactive dashboard allowing support staff to:

Filter queries by status (Open or Closed).

View detailed query information.

Close selected queries, automatically recording the date_closed in the database.

Data Persistence: Utilizes MySQL to store all user and query data reliably.

Data Loading: Includes a dedicated script (queries.py) to bulk-load initial synthetic data from a CSV into the MySQL database.

🛠️ Technologies Used

Frontend/App  -	Streamlit  -	Used for creating the interactive, multi-page web application and user interface.
Backend/Core  -	Python	   -    The primary programming language for the entire application logic and database interaction.
Database      -	MySQL	   -    Used for persistent storage of user accounts and all client query records.
Data Handling -	Pandas	   -    Used for data manipulation, particularly when reading CSV files and filtering query data on the support dashboard.
Security      -	hashlib	   -    Used for securely hashing user passwords before storing them in the database.

⚙️ Setup & Installation

Follow these quick steps to get the application running locally:

1. Prerequisites

Make sure you have a local MySQL Server running.

2. Install Dependencies
Bash

 Install required libraries
pip install streamlit pandas mysql-connector-python

3. Database Initialization
Ensure your MySQL credentials in database.py are correct.

Run the data initialization script to create tables and load sample data:

Bash

python queries.py

4. Run the App
Start the main application using Streamlit:

Bash

streamlit run mainpage.py



✨ Features
Role-Based Access: Separate login for Client and Support users.

Query Submission: Clients can easily submit new tickets.

Support Dashboard: Allows support staff to filter queries by Open or Closed status.

Query Resolution: Support staff can select a query ID and click a button to Close the ticket, recording the date of closure.






