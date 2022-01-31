# Distributed programming project of Université de Paris 2021

# Owner
- LAI Khang Duy
- Lylia DJALI

## How to run
You need to migrate the Django model to PostgreSQL before can record to the database.
```
docker-compose up
docker-compose run django-backend-record-service python3 manage.py migrate
```
