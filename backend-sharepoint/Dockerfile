
FROM python:3.9


WORKDIR /app


COPY requirements.txt requirements.txt


RUN pip install --no-cache-dir --upgrade -r requirements.txt


COPY . /app


CMD ["fastapi", "run", "main.py", "--port", "3002"]