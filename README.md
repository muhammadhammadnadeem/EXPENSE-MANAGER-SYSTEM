# Expense Manager

A personal finance tracker built with Python and Django. Users can register, record income and expenses, categorize expenses, and view a dashboard with totals and balance.

## Features

- User registration and login
- Add, view, and delete expenses
- Add, view, and delete income
- Dashboard showing total income, total expenses, and balance
- User-specific records protected by Django login requirements
- MySQL database configuration

## Tech stack

- Python
- Django
- MySQL
- HTML templates

## Setup (Windows PowerShell)

1. Install Python and MySQL. Create a database:

   ```sql
   CREATE DATABASE expense_manager;
   ```

2. Open PowerShell in this project folder and create a virtual environment:

   ```powershell
   py -m venv venv
   .\venv\Scripts\Activate.ps1
   pip install -r requirements.txt
   ```

3. Set your local database password in the current PowerShell session (replace the example):

   ```powershell
   $env:DB_USER = "root"
   $env:DB_PASSWORD = "your-local-mysql-password"
   $env:DJANGO_SECRET_KEY = "replace-with-a-long-random-secret"
   ```

4. Apply migrations and create an admin account:

   ```powershell
   python manage.py migrate
   python manage.py createsuperuser
   ```

5. Start the development server:

   ```powershell
   python manage.py runserver
   ```

6. Open http://127.0.0.1:8000/ in your browser.

## Important security notes

- This repository is for learning and portfolio demonstration. Do not use Django's development server for production hosting.
- Keep passwords and secret keys out of GitHub. Configure environment variables for your own machine or deployment.
- `DEBUG` is enabled by default for local development. Set `DJANGO_DEBUG=False` and configure `DJANGO_ALLOWED_HOSTS` before deployment.
- The local database file and virtual environment are intentionally excluded from the repository.
