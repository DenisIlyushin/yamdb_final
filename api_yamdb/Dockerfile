FROM python:3.7-slim

LABEL author='DenisIlyushin'
LABEL version=1.0
LABEL description="Sprint_12 learning docker container"

WORKDIR /app

COPY requirements.txt .

RUN pip3 install -r /app/requirements.txt --no-cache-dir

COPY ./ .

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]
