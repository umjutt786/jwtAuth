# JWT Authentication with Laravel

This is a Laravel project implementing JWT (JSON Web Token) authentication.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)

## Prerequisites

Make sure you have the following installed:

- PHP 8.3
- Composer
- Laravel 11
- MySQL (or another database)

## Installation

1. **Clone the repository**:

   git clone https://github.com/umjutt786/jwtAuth.git

2. **Navigate to the project directory**:

    cd jwtAuth

3. **Install the required dependencies**:

    composer install

## Configuration

1. **Copy the example environment file**:

    cp .env.example .env
2. **Configure your database settings**:

Open the .env file in your favorite text editor and set your database connection parameters:

    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=your_database_username
    DB_PASSWORD=your_database_password

3. **Generate the application key**:

    php artisan key:generate

4. **Run Migrations**:
    
    php artisan migrate

## Running the Application

    php artisan serve
## API Endpoints

Here are some of the available API endpoints:

### Register

- **Method**: `POST`
- **Endpoint**: `/api/register`
- **Description**: Create a new user account.
- **Request Body**:
  ```json
  {
      "name": "John Doe",
      "email": "john@example.com",
      "password": "yourpassword",
      "password_confirmation": "yourpassword"
  }

### Login

- **Method**: `POST`
- **Endpoint**: `/api/login`
- **Description**: Login.
- **Request Body**:
  ```json
  {
      "email": "john@example.com",
      "password": "yourpassword",
  }







