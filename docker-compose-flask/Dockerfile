FROM python:3.7-alpine
ENV FLASK_APP app.py
ENV FLASK_RUN_HOST 0.0.0.0
RUN mkdir /code
WORKDIR /code
RUN apk add --no-cache gcc musl-dev linux-headers
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY . .
CMD ["flask", "run"]