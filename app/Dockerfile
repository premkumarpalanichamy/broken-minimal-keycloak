FROM python:3.8-slim

LABEL Author Name="Prem Kumar Palanichamy" \
      Author Email="premkumaropedia@gmail.com" \
      desc="This is docker image rework for keycloack issue 

ENV PYTHONUNBUFFERED=1
RUN mkdir /var/www
COPY requirements.txt /var/www/
RUN cd /var/www && \
    python3 -m pip install -r requirements.txt
COPY app.py .

ENTRYPOINT ["gunicorn", "app:app", "--bind=0.0.0.0:8000", "--workers=4", "--log-level=debug", "--reload"]