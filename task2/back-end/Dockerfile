FROM ubuntu:latest

RUN apt-get update

RUN apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

# Eliminate EXTERNALLY-MANAGED file to use pip and install packages like flask
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

RUN pip install flask

WORKDIR /app

COPY ./api.py /app

# Make port 5252 available outside this container
EXPOSE 5252

CMD [ "python3", "api.py" ]