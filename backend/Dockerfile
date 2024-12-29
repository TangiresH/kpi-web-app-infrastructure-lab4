FROM python:3.9-slim

RUN apt-get update && apt-get install -y \
    libpq-dev \
    build-essential

WORKDIR /app

COPY . /app

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
