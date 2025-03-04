# Technical Documentation for Blog CRUD 1 Project
## Introduction
### This is a simple blog CRUD (Create, Read, Update, Delete) application built using Django. It allows users to create, view, edit, and delete blog posts. This application demonstrates the usage of Django's basic features such as models, views, forms, and templates.

## Installation
### 1. Clone the repository:
git clone
### 2. Create a virtual environment:
python3 -m venv venv
### 3. Activate the virtual environment:
On Windows
venv\Scripts\activate
On macOS/Linux
source venv/bin/activate
### 4. Install the required dependencies:
pip install -r requirements.txt
### 5. Run migrations to set up the database:
python manage.py migrate
### 6. Create a superuser to access the Django admin panel:
python manage.py createsuperuser
### 7. Run the server:
python manage.py runserver
### 8. Access the application at http://127.0.0.1:8000/.

## Functionality
### Models
### The application has a Post model that defines the following fields:

### title: A CharField representing the title of the post.
### content: A TextField representing the content of the post.
### created_at: A DateTimeField representing when the post was created.
### updated_at: A DateTimeField representing when the post was last updated.
### Views
### The views for the blog handle the following actions:

### Post List (post_list): Displays a list of all blog posts.
### Create Post (post_create): Allows the user to create a new post.
### Edit Post (post_update): Allows the user to edit an existing post.
### Delete Post (post_delete): Allows the user to delete a post.
### Templates
### The templates are located in the blog/templates/blog directory.

### post_list.html: Displays the list of blog posts with options to edit or delete them.
### post_form.html: Displays the form for creating or editing a post.
### URLs
### The application has the following URL patterns:

### / (GET): Displays the list of posts.
### /post/new/ (GET, POST): Allows creating a new post.
### /post/<int:pk>/edit/ (GET, POST): Allows editing an existing post.
### /post/<int:pk>/delete/ (GET): Allows deleting a post.