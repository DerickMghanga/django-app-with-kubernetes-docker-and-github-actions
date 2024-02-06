FROM python:3.12.1-slim

COPY . /app
WORKDIR /app

RUN python3 -m venv /opt/venv

RUN /opt/venv/bin/pip install pip --upgrade

# This image will run on a Linux machine not Windows
RUN /opt/venv/bin/pip install -r requirements.txt

# make the entrypoint file executable for users
RUN chmod +x entrypoint.sh

# Execute the file and run in Production server
CMD ["/app/entrypoint.sh"]
