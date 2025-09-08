FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

RUN pip3 install --no-cache-dir flask

WORKDIR /app
COPY ./api.py /app/api.py

CMD ["python3", "api.py"]
