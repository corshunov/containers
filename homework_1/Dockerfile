FROM alpine:3.9

MAINTAINER Aleksandr Korshunov <korshunov.sasha@gmail.com> 

RUN apk update && apk upgrade && apk add python3

RUN mkdir /container_data/
WORKDIR /container_data/

COPY ./requirements.txt ./app.py ./

RUN python3 -m pip install -r requirements.txt

EXPOSE 5000

ENTRYPOINT ["python3", "app.py"]
