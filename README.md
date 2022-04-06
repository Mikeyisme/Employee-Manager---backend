# Employee Manager Back-end

This is an api for the Employee Manager system built with the Django REST Framework.

## Running Locally

1. Clone this repo
1. cd into this repo
1. Create a python virtual environment: `python -m venv venv`
1. Activate virutal environment: `source venv/bin/activate`
1. `pip install -r requirements.txt`
1. `python manage.py runserver`

## Schema

**Task**

* user_id: ForeinKey
* title: required
* description: default=''
* completed: boolean
* due_date: nullable
* created_at
* updated_at

**Tag**

* text: CharField(max_length=25)
* color: CharField(max_length=6)
* *many to many relationship with Task*

**List**

* user_id
* name
* created_at
* updated_at

**ListItem**

* list_id
* text
* created_at
* updated_at

**User**

* email (unique, used for login)
* password

**UserProfile**

* user_id
* first_name
* last_name
* image
* fb_profile
* twitter_profile
* linkedin_profile
* website

**Project**

* user_id
* title
* description
* created_at
* updated_at
* due_date (for version 2)

## API

**/users**

* GET
* POST

**/users/:id**

* GET
* PATCH
* DELETE

**/users/:id/tasks**

* GET
* POST

**/users/:id/tasks/:task_id**

* GET
* PATCH
* DELETE

**/users/:id/lists**

* GET
* POST

**/users/:id/lists/:list_id**

* GET
* PATCH
* DELETE

**/users/:id/lists/:list_id/list-items**

* POST

**/users/:id/list-items/:item_id**

* PATCH
* DELETE

**/tasks**

* GET

**/tasks/:id**

* GET
