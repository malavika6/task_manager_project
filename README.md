Certainly! Here's how you can update the README.md file in your project to include instructions for setting up MSSQL:

```markdown
# Django Project Setup

Here’s a guide to setting up your Django project locally:

## Prerequisites

- Python installed on your system
- Pip installed on your system (Python package installer)
- Git installed on your system
- Optional: Virtual environment (recommended)

## Step-by-Step Setup

###  Clone the Project Repository

1. Open a terminal or command prompt.
2. Navigate to the directory where you want to clone the project.
3. Run the following command to clone the repository:

   ```bash
   git clone https://github.com/TrusttechItSolutions/Cyprus_website_revamp.git
   ```



###  Install Project Dependencies

1. Install Python dependencies using pip:

   ```bash
   pip install -r requirements.txt
   ```

2. Apply migrations to set up the database:

   ```bash
   python manage.py migrate
   ```

3. Create a superuser (admin) account:

   ```bash
   python manage.py createsuperuser
   ```

###  Setting up MSSQL

1. Install the required packages:

   ```bash
   pip install django-pyodbc-azure
   ```

2. Configure Database Settings:

   In your Django project's `settings.py` file, configure the database settings to use MSSQL. Replace the database settings with the following:

   ```python
   DATABASES = {
       'default': {
           'ENGINE': 'sql_server.pyodbc',
           'NAME': 'your_database_name',
           'USER': 'your_database_user',
           'PASSWORD': 'your_database_password',
           'HOST': 'your_database_server',
           'PORT': 'your_database_port',
           'OPTIONS': {
               'driver': 'ODBC Driver 17 for SQL Server',
           },
       }
   }
   ```

   Replace `'your_database_name'`, `'your_database_user'`, `'your_database_password'`, `'your_database_server'`, and `'your_database_port'` with your actual database credentials.

3. Install ODBC Driver:

   Download and install the ODBC Driver for SQL Server appropriate for your operating system from the [Microsoft Download Center](https://docs.microsoft.com/en-us/sql/connect/odbc/download-odbc-driver-for-sql-server).

4. Configure ODBC Data Source:

   Configure an ODBC Data Source using the ODBC Driver installed in the previous step.

5. Test the Connection:

   After configuring the ODBC Data Source, test the connection to ensure it's working correctly.

###  Serve the Application

Start the Django development server:

```bash
python manage.py runserver
```

Access your Django project at [http://localhost:8000](http://localhost:8000).

### Optional: Using Virtual Environment

If you prefer to use a virtual environment, here are the additional steps:

1. Install virtualenv:

   ```bash
   pip install virtualenv
   ```

2. Create a virtual environment:

   ```bash
   virtualenv env
   ```

3. Activate the virtual environment:

   - On Windows:

     ```bash
     .\env\Scripts\activate
     ```

   - On macOS/Linux:

     ```bash
     source env/bin/activate
     ```

Then continue with the steps mentioned above for cloning the repository and setting up the project.

This setup should get your Django project up and running smoothly on your local machine! Let me know if you need further assistance.
```

Feel free to copy and paste this into your README.md file, adjusting any project-specific details as needed!
