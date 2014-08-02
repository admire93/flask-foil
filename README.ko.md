flask-foil
==========

flask boilerplate 생성기.

## 설치

    $ git clone https://github.com/admire93/flask-foil.git
    $ cd flask-foil
    $ pip install . # 또는 python setup.py install

## 개요

flask, sqlalchemy, flask-script로 구성되어있는 프로젝트를 시작해보세요.

    $ foil gen
    $ vim gen.ini
    $ foil start
    $ manager.py -c exam.cfg.py runserver

## 사용방법

우선 프로젝트를 시작하기위해서 설정파일을 생성합니다.

    $ mkdir my_project
    $ cd my_project
    $ foil gen

현재 디렉토리에 `gen.ini`가 생성되게되는데, `gen.ini`에 정보를 채워넣어주시면됩니다. `gen.ini`는 프로젝트이름, 작성자의 이메일, 이름 등의 다양한 설정을 포함하고있습니다.

    $ cat gen.ini
    [foil]
    project_name =
    database_url =
    project_root =
    author_name =
    author_email =

이 설정 변수들은 다음과 같은 규칙을 따릅니다.

 - `project_name`은 [pep8][pep8]에 명시되어있는 규칙을 따릅니다.
 - sqlalchemy의 엔진을 생성하기위해서 `database_url`는 반드시 필요합니다.
 - `databalse_url` 스키마는 [URI scheme][uri]로 작성하면됩니다.  (ie. `postgresql://username:password@host.com:5432/dbname`.)
 - `project_root`는 반드시 `/`로 끝나야합니다. (ie. o `/Users/admire93/my_project/`, x `/Users/admire93/my_project`)

[pep8]: http://legacy.python.org/dev/peps/pep-0008/#package-and-module-names
[uri]: http://en.wikipedia.org/wiki/URI_scheme
