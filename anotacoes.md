# API features:

https://github.com/LondonAppDeveloper/c2-recipe-app-api-2

* User Authentication
* Creating objects
* Filtering & sorting objects
* Uploading & viewing images


## App Design

* Intro to TDD
* System Setup
* Project Setup
* Configure Github Actions
* TDD with Django
* Configure Database
* Create User Model
* Setup Django Admin
* API Documentation
* Build User API
* Build Recipe API
* Build Tags API
* Build Ingredients API
* Recipe Image API
* Implement Filtering
* Deploy to AWS


# Techonologies

## Django

* URL Mappings
* Object Relational Mapper
* Admin Site

## Github Actions

* Automation
* Testing and Linting



# Project Structure

* `app/` - Django project
* `app/core/` - Code shared between multiple apps
* `app/user/` - User related code
* `app/recipe/` - Recipe related code


* Create a new project
* Using Docker with Django
* Setup new Django project
* Linting and Testing
* Using Docker Compose


# Why use Docker?

* Consistent dev and prod environment
* Easier collaboration
    * Different version of Python
    * Different version of database
    * Different version of SDK
* Capture all dependencies as code
    * Python requirements
    * Operating system dependencies
* Easier cleanup

## How we'll use Docker

* Define Dockerfile
* Create Docker Compose configuration
* Run all commands via Docker Compose

## Docker on Github Actions

Authenticate with Docker Hub

On Github repository, click Settings > Secrets > Actions and click on **New repository secret**


## Linting

```
docker-compose build
docker-compose run --rm app sh -c "flake8"
```

## Testing

```
python manage.py test
```

## Creating Project

```
django-admin startproject app .
```

## Test classes

* SimpleTestCase
    * No database integration
    * Useful if no database is required for your test
    * Save time executing tests

* TestCase
    * Database integration
    * Useful for testing code that uses the database

## Mocking

* Override or change behaviour of dependencies
* Avoid unintended side effects
* Isolate code being tested

### Why use mocking?

* Avoid relying on external services
    * Can't guarantee they will be available
    * Makes tests unpredictable and inconsistent

* Avoid unintended consequences
    * Accidentally sending emails
    * Overloading external services

Example:

```
register_user()
create_in_db()
send_welcome_email()
```

* Prevent email being send
* Ensure `send_welcome_email()` called correctly

### How to mock code?

* Use `unittest.mock`
    * `MagicMock/Mock` - Replace real objects
    * `patch` - Overrides code for tests


# Testing Web Requests

## Testing APIs

* Make actual requests
* Check result

## Django REST framework APIClient

* Based on the Django's TestClient
* Make requests
* Check result
* Override authentication

## Using the APIClient

* Import `APIClient`
* Create client
* Make request
* Check result

 