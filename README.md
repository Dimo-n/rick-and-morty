# Rick and Morty


### How to run
- Create venv: `python -m venv venv`
- Activate it: `python venv\Scripts\activate`
- Install requirements: `pip install -r requirements.txt`
- Run migrations: `python manage.py migrate`
- Run Redis Server: `docker run -d -p 6379:6379 redis`
- Run Celery worker for tasks  handling: `celery -A rick_and_morty_api worker -l INFO --pool=solo`
- Run Celery Beat for task scheduling: `celery -A rick_and_morty_api beat -l INFO --scheduler django_celery_beat.schedulers:DatabaseScheduler`
- Create schedule for running sync in DB from admin panel
- Run app `python manage.py  runserver`
