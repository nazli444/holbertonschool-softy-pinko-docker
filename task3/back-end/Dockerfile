FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

# Avoid EXTERNALLY-MANAGED environment breakages on newer Ubuntu images if required
RUN pip3 install --break-system-packages flask
RUN pip3 install --break-system-packages flask-cors

WORKDIR /app
COPY ./api.py /app/api.py

EXPOSE 5252

CMD ["python3", "api.py"]
