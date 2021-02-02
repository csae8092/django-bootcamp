# django-bootcamp

## python
use e.g. https://www.anaconda.com/ (windows)

## editor
* my choice: https://code.visualstudio.com/

## offical django-tutorial

https://docs.djangoproject.com/en/3.1/intro/tutorial01/

* all code should be in version-control -> set up git & github-repo
* use a virtual environment (conda or virtualenv)
  * https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands
  
  
## run custom project locally

you'll need to have a postgres-db set up locally

### set up app locally
* clone https://github.com/acdh-oeaw/mmp
* install required packages (`pip install -r requirements.txt`)
* create a postgresql db `mmp`
* create a custom settings-file e.g. `settings/pg_local.py`
* add the db-credentials to connect to your db
* run migrations, e.g. `python manage.py migrate --settings=djangobaseproject/settings.pg_local
* create a superuser
* start the dev server
* try to create/edit/delete objects

### restore db-backup and connect to it
* request a copy of a populated mmp-db from @csae8092
* create a postgresql db `mmp` (maybe you'll need to delete the previous one)
* restore backup
* start the dev server and see if everything works
