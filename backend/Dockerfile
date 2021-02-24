FROM alpine
MAINTAINER amhendley@gmail.com<Andrew M Hendley>

RUN mkdir -p /app

COPY / /app/

WORKDIR /app

RUN apk add gcc g++ make musl-dev libffi libffi-dev libuv python3 python3-dev py3-pip
RUN ln -s /usr/bin/python3 /usr/bin/python
RUN pip install -r requirements.txt

EXPOSE 8000

CMD [ "python", "main.py" ]
