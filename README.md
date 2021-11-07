### Django 101

##### Basic poll application.

- The outer **Django101**/ root directory is a container for your project. 
- [manage.py](manage.py): A command-line utility that lets you interact with this Django project in various ways.
- The inner **Django101**/ directory is the actual Python package for project.
- [Django101/__init__.py](./Django101/__init__.py): An empty file that tells Python that this directory should be considered a Python package.
- [Django101/settings.py](./Django101/settings.py): Settings/configuration for this Django project.
  - DATABASES:
    - ENGINE – Either 'django.db.backends.sqlite3', 'django.db.backends.postgresql', 'django.db.backends.mysql', or 'django.db.backends.oracle'. Other backends are also available. 
    - NAME – The name of your database. If you’re using SQLite, the database will be a file on your computer; in that case, NAME should be the full absolute path, including filename, of that file. The default value, BASE_DIR / 'db.sqlite3', will store the file in your project directory.
- [Django101/urls.py](./Django101/urls.py): The URL declarations for this Django project; a “table of contents” of your Django-powered site.
- [Django101/asgi.py](./Django101/asgi.py): An entry-point for ASGI-compatible web servers to serve your project.
- [Django101/wsgi.py](./Django101/wsgi.py): An entry-point for WSGI-compatible web servers to serve your project. See How to deploy with WSGI for more details.

#### The development server automatically reloads Python code for each request as needed. You don’t need to restart the server for code changes to take effect. However, some actions like adding files don’t trigger a restart, so you’ll have to restart the server in these cases.

### Projects vs. apps
An app is a Web application that does something – e.g., a Weblog system, a database of public records or a small poll app. A project is a collection of configuration and apps for a particular website. A project can contain multiple apps. An app can be in multiple projects.

##### To call the view, we need to map it to a URL - and for this we need a URLconf.

##### The include() function allows referencing other URLconfs. Whenever Django encounters include(), it chops off whatever part of the URL matched up to that point and sends the remaining string to the included URLconf for further processing

#### The path() function is passed four arguments, two required: route and view, and two optional: kwargs, and name. At this point, it’s worth reviewing what these arguments are for.
- **route** is a string that contains a URL pattern. When processing a request, Django starts at the first pattern in urlpatterns and makes its way down the list, comparing the requested URL against each pattern until it finds one that matches.
- When Django finds a matching pattern, it calls the specified **view** function with an HttpRequest object as the first argument and any “captured” values from the route as keyword arguments. We’ll give an example of this in a bit.
- **kwargs**: Arbitrary keyword arguments can be passed in a dictionary to the target view. We aren’t going to use this feature of Django in the tutorial.
- **name**: Naming your URL lets you refer to it unambiguously from elsewhere in Django, especially from within templates. This powerful feature allows you to make global changes to the URL patterns of your project while only touching a single file. .

### Model
A model is the single, definitive source of information about your data. It contains the essential fields and behaviors of the data you’re storing. Django follows the DRY Principle. The goal is to define your data model in one place and automatically derive things from it.

#### To include the app in our project, we need to add a reference to its configuration class in the INSTALLED_APPS setting. The PollsConfig class is in the polls/apps.py file, so its dotted path is 'polls.apps.PollsConfig'. Edit the mysite/settings.py file and add that dotted path to the INSTALLED_APPS setting. It’ll look like this:

### makemigrations vs migrate
#### Change your models (in models.py).
#### Run python manage.py makemigrations to create migrations for those changes
#### Run python manage.py migrate to apply those changes to the database.

**py manage.py createsuperuser** used to create superusers
