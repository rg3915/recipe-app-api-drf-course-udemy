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
docker-compose run --rm app sh -c "python manage.py test"
```

## Creating Project

```
docker-compose run --rm app sh -c "django-admin startproject app ."
```