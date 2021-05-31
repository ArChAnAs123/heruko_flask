web: python app.py $PORT
web: gunicorn app:app
clock: python autoscale.py
web: waitress-serve --port=$PORT --threads=${WEB_CONCURRENCY:-2} --call 'app:app'
