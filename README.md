### Django 101

##### Basic poll application.

- The outer **Django101**/ root directory is a container for your project. 
- [manage.py](manage.py): A command-line utility that lets you interact with this Django project in various ways.
- The inner **Django101**/ directory is the actual Python package for project.
- [Django101/__init__.py](./Django101/__init__.py): An empty file that tells Python that this directory should be considered a Python package.
- [Django101/settings.py](./Django101/settings.py): Settings/configuration for this Django project. 
- [Django101/urls.py](./Django101/urls.py): The URL declarations for this Django project; a “table of contents” of your Django-powered site.
- [Django101/asgi.py](./Django101/asgi.py): An entry-point for ASGI-compatible web servers to serve your project.
- [Django101/wsgi.py](./Django101/wsgi.py): An entry-point for WSGI-compatible web servers to serve your project. See How to deploy with WSGI for more details.

#### The development server automatically reloads Python code for each request as needed. You don’t need to restart the server for code changes to take effect. However, some actions like adding files don’t trigger a restart, so you’ll have to restart the server in these cases.

### Projects vs. apps
An app is a Web application that does something – e.g., a Weblog system, a database of public records or a small poll app. A project is a collection of configuration and apps for a particular website. A project can contain multiple apps. An app can be in multiple projects.


