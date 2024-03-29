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

you'll need to have a postgres-db set up locally and [GDAL](https://docs.djangoproject.com/en/3.1/ref/contrib/gis/install/geolibs/) installed


### set up app locally
* clone https://github.com/acdh-oeaw/mmp
* install required packages (`pip install -r requirements.txt`)
* create a postgresql db `mmp`
* create postigs extension
* create a custom settings-file e.g. `settings/pg_local.py`
* add the db-credentials to connect to your db
* run migrations, e.g. `python manage.py migrate --settings=djangobaseproject.settings.pg_local
* create a superuser
* start the dev server
* try to create/edit/delete objects

### restore db-backup and connect to it
* request a copy of a populated mmp-db from @csae8092
* create a postgresql db `mmp` (maybe you'll need to delete the previous one)
* restore backup
* start the dev server and see if everything works


## write jupyter notebooks to import data

after restoring the dump, lets delete the database and start from a new one

* apply migrations
* click through the app and try to create/edit/delete objects

### set up django-extension and jupyter notebook
* see e.g https://dev.to/davitovmasyan/how-to-use-the-django-shell-in-jupyter-notebook-ofn
* install `django-extensions` 
* install `jupyter` and `notebook` (pip install jupyter notebook)
* try to run `python manage.py shell_plus --notebook --settings=djangobaseproject.settings.{my_settings_file}

### import scripts

* start with import of Orte
* next "Autor"
* next "Text"

Tips: 
* use pandas to parse csv files into pd.DataFrame
* use something like `for i, row in df.iterrows():` to iterate through rows
* use `SomeClass.objects.get_or_create()` method to write idempodent scripts (you can run then several times with the same output)
* see e.g. https://github.com/acdh-oeaw/daacda-go-digital/blob/master/import__database_list_2018_06_04.ipynb for an example



