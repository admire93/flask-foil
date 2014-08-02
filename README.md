flask-foil
==========

generate flask boilerplate.

## Installation

todo

## Overview

Start flask project contain sqlalchemy, flask-script.

    $ foil gen
    $ vim gen.ini
    $ foil start
    $ manager.py -c exam.cfg.py runserver

## Usage

first, generate configuration file to start project.

    $ mkdir my_project
    $ cd my_project
    $ foil gen

it generate `gen.ini` in current directory and edit `gen.ini` with your favorite editor.
`gen.ini` contains various configuration of project such as project name, author email, name, etc.

    $ cat gen.ini
    [foil]
    project_name =
    database_url =
    project_root =
    author_name =
    author_email =

these configuration variables follow rules below.

 - To use a module name. `project_name` have to follow [pep8 convention][pep8].
 - To create sqlalchemy engine, `database_url` must be required.
 - `databalse_url` scheme follow [URI scheme][uri]. (ie. `postgresql://username:password@host.com:5432/dbname`.)
 - `project_root` must end with `/`. (ie. o `/Users/admire93/my_project/`, x `/Users/admire93/my_project`)

[pep8]: http://legacy.python.org/dev/peps/pep-0008/#package-and-module-names
[uri]: http://en.wikipedia.org/wiki/URI_scheme
