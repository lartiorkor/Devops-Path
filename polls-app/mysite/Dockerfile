FROM python:3.8-alpine

COPY requirements.txt /app/
COPY . /app/

WORKDIR /app

RUN pip install -r requirements.txt
RUN pip install django-prometheus
RUN python manage.py migrate

CMD [ "python",  "manage.py", "runserver"]