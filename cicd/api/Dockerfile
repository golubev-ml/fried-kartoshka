FROM python:3.9

RUN apt update && \
    pip install django==3.1.4 && \
    pip install djangorestframework==3.12.2 && \
    pip install markdown==3.3.3 && \
    pip install django-filter==2.4.0 && \
    pip install gunicorn==20.0.4 && \
    pip install psycopg2-binary==2.8.6

COPY drf /fried-kartoshka

WORKDIR /fried-kartoshka

EXPOSE 8000

CMD ["gunicorn", "api.wsgi", "-w", "1", "--bind" , "0.0.0.0:8000"]