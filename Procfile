web: gunicorn --bind 0.0.0.0:$PORT app:app
web: python app.py $PORT
clock: python autoscale.py
web: waitress-serve --port=$PORT --threads=${WEB_CONCURRENCY:-2} --call 'app:app'
