FROM python:3.7
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
RUN pip install gunicorn
ENV PORT=8085
CMD exec gunicorn --bind :$PORT --workers 1 --threads 8 main:app