web: bin/start-nginx gunicorn -c gunicorn.conf django_app.wsgi:application
worker: REMAP_SIGTERM=SIGQUIT celery -A django_app worker -l error
release: python manage.py migrate
