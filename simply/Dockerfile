FROM --platform=linux/amd64 python:3.11-bullseye
ENV PYTHONUNBUFFERED=1
WORKDIR /simply
COPY requirements.txt . 
RUN pip3 install -r requirements.txt
COPY . .
# CMD python manage.py runserver 0.0.0.0:8000
CMD ["gunicorn", "simply.wsgi", "--bind", "0.0.0.0:8000"]