FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y python3
RUN apt-get install -y python3-pip

RUN rm -rf /var/lib/apt/lists/*

RUN find /usr -name EXTERNALLY-MANAGED -delete

RUN pip3 install flask
RUN pip3 install flask-cors


WORKDIR /app
COPY task3/back-end/api.py /app/api.py
EXPOSE 5252
CMD ["python3", "api.py"]