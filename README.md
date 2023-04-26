# DRF Cinema with Docker

API of basic cinema logic using Django REST framework


## Using DRF & PostgreSQL:
Python 3 & PostgresSQL must be installed before

Create db using pgAdmin
```shell
git clone https://github.com/ada-krav/DRF_cinema_with_docker
cd cinema_service
python -m venv venv
venv\Scripts\activate (on Windows)
source venv/bin/activate (on macOS)
pip install -r requirements.txt

export DJANGO_SECRET_KEY=<use your DJANGO_SECRET_KEY>
export DEBUG=<True or False>
export ALLOWED_HOSTS=<use your ALLOWED_HOSTS>
export DB_HOST=<use your DB_HOST>
export DB_NAME=<use your DB_NAME>
export DB_USER=<use your DB_USER>
export DB_PASSWORD=<use your DB_PASSWORD>

python manage.py migrate
python manage.py runserver
```
## Using Docker:
Python 3 & Docker must be installed

```shell
git clone https://github.com/ada-krav/DRF_cinema_with_docker
cd cinema_service
docker-compose build
docker-compose up
```


## How to get access in both cases:

*  create new user - http://localhost:8000/api/user/register/
*  get JWT Token - http://localhost:8000/api/user/token/

## Features
* JWT authenticated 

* Admin panel: /admin/

* Documentation: /api/doc/swagger/

* Managing orders and tickets

* Creating movies with genres, actors

* Creating cinema 

* Adding movie sessions

* Filtering movies and movie sessions