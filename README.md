# Newspaper Blog

Welcome to the **Newspaper Blog** project! This is a Django-based web application designed to provide a platform for users to read and share  articles.

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication system (registration, login, logout)
- Create, read, update, and delete (CRUD) functionality for blog posts
- Responsive design using HTML and CSS
- Admin interface for managing users and posts

## Project Structure

The project is organized as follows:

```
Newspaper-blog/
├── accounts/               # Django app for user authentication
│   ├── migrations/         # Database migrations for accounts app
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
├── blog/                   # Django app for blog functionality
│   ├── migrations/         # Database migrations for blog app
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
├── blog_project/           # Project configuration
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── static/                 # Static files (CSS, JavaScript, images)
├── templates/              # HTML templates
├── .gitignore              # Git ignore file
├── Procfile                # For deployment configurations
├── README.md               # Project documentation
├── manage.py               # Django management script
└── requirements.txt        # Python package dependencies
```

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Mashon8945/Newspaper-blog.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd Newspaper-blog
   ```

3. **Create a virtual environment**:

   ```bash
   python -m venv venv
   ```

4. **Activate the virtual environment**:

   - On Windows:

     ```bash
     venv\Scripts\activate
     ```

   - On macOS/Linux:

     ```bash
     source venv/bin/activate
     ```

5. **Install the required packages**:

   ```bash
   pip install -r requirements.txt
   ```

6. **Apply database migrations**:

   ```bash
   python manage.py migrate
   ```

7. **Create a superuser** (for accessing the admin interface):

   ```bash
   python manage.py createsuperuser
   ```

8. **Collect static files**:

   ```bash
   python manage.py collectstatic
   ```

## Usage

1. **Run the development server**:

   ```bash
   python manage.py runserver
   ```

2. **Access the application**:

   Open your web browser and navigate to `http://127.0.0.1:8000/`.

3. **Admin Interface**:

   To access the Django admin interface, go to `http://127.0.0.1:8000/admin/` and log in with the superuser credentials you created earlier.

## Deployment

To deploy this application to a platform like Heroku, follow these steps:

1. **Install the Heroku CLI**:

   Download and install the Heroku CLI from [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli).

2. **Log in to Heroku**:

   ```bash
   heroku login
   ```

3. **Create a new Heroku app**:

   ```bash
   heroku create your-app-name
   ```

4. **Add Heroku Postgres** (for the database):

   ```bash
   heroku addons:create heroku-postgresql:hobby-dev
   ```

5. **Set environment variables**:

   ```bash
   heroku config:set SECRET_KEY='your_secret_key'
   heroku config:set DEBUG=False
   ```

6. **Push the code to Heroku**:

   ```bash
   git push heroku main
   ```

7. **Apply database migrations on Heroku**:

   ```bash
   heroku run python manage.py migrate
   ```

8. **Create a superuser on Heroku**:

   ```bash
   heroku run python manage.py createsuperuser
   ```

9. **Collect static files on Heroku**:

   ```bash
   heroku run python manage.py collectstatic
   ```

10. **Open the deployed app**:

    ```bash
    heroku open
    ```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature-name`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/your-feature-name`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.