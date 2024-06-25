# Flask-Admin

The project was recently moved into its own organization. Please update
your references to *git@github.com:flask-admin/flask-admin.git*.

[![image](https://d322cqt584bo4o.cloudfront.net/flask-admin/localized.svg)](https://crowdin.com/project/flask-admin)

[![image](https://github.com/flask-admin/flask-admin/actions/workflows/test.yaml/badge.svg)](https://github.com/flask-admin/flask-admin/actions/workflows/test.yaml)

## Introduction

Flask-Admin is a batteries-included, simple-to-use
[Flask](http://flask.pocoo.org/) extension that lets you add admin
interfaces to Flask applications. It is inspired by the *django-admin*
package, but implemented in such a way that the developer has total
control of the look, feel and functionality of the resulting
application.

Out-of-the-box, Flask-Admin plays nicely with various ORM\'s, including

-   [SQLAlchemy](http://www.sqlalchemy.org/),
-   [MongoEngine](http://mongoengine.org/),
-   [pymongo](http://api.mongodb.org/python/current/) and
-   [Peewee](https://github.com/coleifer/peewee).

It also boasts a simple file management interface and a [redis
client](http://redis.io/) console.

The biggest feature of Flask-Admin is flexibility. It aims to provide a
set of simple tools that can be used for building admin interfaces of
any complexity. So, to start off with you can create a very simple
application in no time, with auto-generated CRUD-views for each of your
models. But then you can go further and customize those views & forms as
the need arises.

Flask-Admin is an active project, well-tested and production ready.

## Examples

Several usage examples are included in the */examples* folder. Please
add your own, or improve on the existing examples, and submit a
*pull-request*.

To run the examples in your local environment:

    1. Clone the repository::

          git clone https://github.com/flask-admin/flask-admin.git
          cd flask-admin

    2. Create and activate a virtual environment::

          virtualenv env -p python3
          source env/Scripts/activate

    3. Install requirements::

          pip install -r examples/sqla/requirements.txt

    4. Run the application::

          python examples/sqla/run_server.py

## Documentation

Flask-Admin is extensively documented, you can find all of the
documentation at <https://flask-admin.readthedocs.io/en/latest/>.

The docs are auto-generated from the *.rst* files in the */doc* folder.
So if you come across any errors, or if you think of anything else that
should be included, then please make the changes and submit them as a
*pull-request*.

To build the docs in your local environment, from the project directory:

    tox -e docs-html

And if you want to preview any *.rst* snippets that you may want to
contribute, go to <http://rst.ninjs.org/>.

## Installation

To install Flask-Admin, simply:

    pip install flask-admin

Or alternatively, you can download the repository and install manually
by doing:

    git clone git@github.com:flask-admin/flask-admin.git
    cd flask-admin
    python setup.py install

## Tests

Test are run with *pytest*. If you are not familiar with this package
you can get some more info from [their website](https://pytest.org/).

To run the tests, from the project directory, simply:

    pip install -r requirements-dev.txt
    pytest

You should see output similar to:

    .............................................
    ----------------------------------------------------------------------
    Ran 102 tests in 13.132s

    OK

For all the tests to pass successfully, you\'ll need Postgres & MongoDB
to be running locally. For Postgres:

    > psql postgres
    CREATE DATABASE flask_admin_test;
    \q

    > psql flask_admin_test
    CREATE EXTENSION postgis;
    CREATE EXTENSION hstore;

If you\'re using Homebrew on MacOS, you might need this:

    # install postgis
    > brew install postgis

    # set up postgresql user
    > createuser -s postgresql
    > brew services restart postgresql

You can also run the tests on multiple environments using *tox*.

## 3rd Party Stuff

Flask-Admin is built with the help of
[Bootstrap](http://getbootstrap.com/),
[Select2](https://github.com/ivaynberg/select2) and
[Bootswatch](http://bootswatch.com/).

If you want to localize your application, install the
[Flask-BabelEx](https://pypi.python.org/pypi/Flask-BabelEx) package.

You can help improve Flask-Admin\'s translations through Crowdin:
<https://crowdin.com/project/flask-admin>
