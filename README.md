# MyBlog - A Modern Blog Platform

MyBlog is a full-featured, responsive blog web application built with Python and the Flask framework. It provides a clean and modern user interface for reading, creating, and managing blog posts, complete with secure user authentication and a database-driven backend.

## Features

* **User Authentication**: Secure user registration and login system. Users can create accounts, log in, and log out.
* **Session Management**: Keeps users logged in using secure sessions.
* **CRUD Functionality for Posts**: Authenticated users can **C**reate, **R**ead, **U**pdate, and **D**elete their own blog posts.
* **Responsive UI**: A modern, mobile-first design built with Bootstrap 5 and a custom stylesheet, ensuring a great experience on any device.
* **Database-Driven**: All user and post data is stored and managed in a MySQL database.
* **Password Hashing**: User passwords are securely hashed and never stored in plain text.

## Technologies Used

* **Backend**: Python, Flask
* **Database**: MySQL
* **ORM**: Flask-SQLAlchemy
* **Authentication**: Flask-Login, Werkzeug (for password hashing)
* **Frontend**: HTML5, CSS3, Bootstrap 5
* **Deployment**: PythonAnywhere

## Local Setup and Installation

To run this project on your local machine, follow these steps:

**1. Clone the repository:**

git clone [https://github.com/YOUR_USERNAME/MyBlog.git](https://github.com/YOUR_USERNAME/MyBlog.git)
cd MyBlog

2. Create and activate a virtual environment:

For Windows
python -m venv env
.\env\Scripts\activate

For macOS/Linux
python3 -m venv env
source env/bin/activate

3. Install the required packages:

pip install -r requirements.txt

4. Set up the MySQL Database:

Create a new database (schema) in MySQL named myblog.

Open the app.py file.

Modify the SQLALCHEMY_DATABASE_URI to match your MySQL credentials:

app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql+pymysql://root:YOUR_PASSWORD@localhost/myblog'

Replace YOUR_PASSWORD with your actual MySQL root password.

5. Create the database tables:

Open a Python terminal in your project directory.

Run the following commands:

from app import app, db
with app.app_context():
    db.create_all()
exit()

6. Run the application:

python app.py

The application will be available at http://127.0.0.1:5000.

**Action Required:** Remember to replace `YOUR_USERNAME` in the clone URL with your actual GitHub username once you've created the repository.
