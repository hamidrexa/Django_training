
[https://www.digitalocean.com/community/tutorials/how-to-install-the-django-web-framework-on-ubuntu-18-04#creating-a-sample-project]

sudo apt-get install python3
python --version
sudo apt-get install -y python3-pip
pip --version
sudo apt install python3-venv
python3.6 -m venv django_venv
source django_venv/bin/activate
pip install django
django-admin --version
django-admin startproject djangoproject .
python manage.py createsuperuser
python manage.py migrate
python manage.py runserver localhost:8000

django description:
djangoproject
superuser: hamidrexa
password: bhamid71

[https://www.digitalocean.com/community/tutorials/how-to-set-up-django-with-postgres-nginx-and-gunicorn-on-ubuntu-18-04]
sudo apt update
sudo apt install python3-pip python3-dev libpq-dev postgresql postgresql-contrib nginx curl
sudo -u postgres psql
CREATE DATABASE mytest;
CREATE USER mytestuser WITH PASSWORD 'password';
ALTER ROLE myprojectuser SET client_encoding TO 'utf8';
ALTER ROLE myprojectuser SET default_transaction_isolation TO 'read committed';
ALTER ROLE myprojectuser SET timezone TO 'UTC';
GRANT ALL PRIVILEGES ON DATABASE mytest TO mytestuser;
pip install gunicorn psycopg2-binary

postgres description:
DATABASE: mytest
USER: mytestuser
PASSWORD: password