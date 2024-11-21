flask User Registration and Login System

A simple Flask web application that allows users to register, log in, and access a dashboard. The application uses SQLite to store user data.

Features

	•	User Registration: Allows new users to create an account.
	•	User Login: Allows registered users to log in using their credentials.
	•	Dashboard: Displays a dashboard page after a successful login.
	•	Logout: Logs users out of the application and redirects to the login page.

Prerequisites

Before running the application, ensure you have the following installed:

	•	Python 3.x
	•	Flask
	•	Flask-SQLAlchemy

Installation

Follow these steps to set up and run the application:

Step 1: Clone the Repository

Clone the project to your local machine using the following command:

git clone https://github.com/yourusername/your-repository-name.git

Step 2: Set Up a Virtual Environment

Navigate to your project directory and create a virtual environment:

cd your-repository-name
python3 -m venv venv

Activate the virtual environment:

	•	For Windows:

venv\Scripts\activate


	•	For macOS/Linux:

source venv/bin/activate



Step 3: Install Dependencies

Install the required dependencies by running:

pip install -r requirements.txt

If you don’t have the requirements.txt file, manually install Flask and Flask-SQLAlchemy:

pip install flask flask_sqlalchemy

Step 4: Set Up the Database

Before running the application, initialize the SQLite database. Add the following code in app.py:

with app.app_context():
    db.create_all()

This will create the users.db database and tables.

Step 5: Run the Application

Run the Flask application by executing the following:

python app.py

The server will start running at http://127.0.0.1:5000/. Visit this URL in your browser.

Project Structure

The project directory structure should look like this:

/your_project
    /app.py                    # Main Flask application file
    /templates
        /register.html         # Registration form template
        /login.html            # Login form template
        /dashboard.html        # User dashboard template
    /static
        /styles.css            # Optional CSS for styling
    /requirements.txt          # List of dependencies
    /users.db                  # SQLite database file (auto-created)

Routes

	•	/register: Displays the registration form and allows new users to register.
	•	/login: Displays the login form and allows users to log in.
	•	/dashboard: Displays the user dashboard after a successful login.
	•	/logout: Logs the user out and redirects to the login page.

Notes

	•	The users.db file will be created automatically the first time you run the app.
	•	Password Hashing: For security reasons, passwords should not be stored in plain text. In a production app, consider using a password hashing library like Werkzeug to securely hash user passwords before storing them in the database.
	•	Development Server: Flask’s built-in server is for development purposes only. For production use, you should consider using a production-ready server like Gunicorn.

License

This project is licensed under the MIT License – see the LICENSE file for details.

This README.md file covers the essential steps to set up, install, and run the Flask registration and login system. It also includes instructions for initial database setup, starting the server, and information about the project structure.

Let me know if you need further customization or additional features!