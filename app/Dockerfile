FROM ubuntu:16.04


RUN apt-get update -y && \
    apt-get install -y python-pip python-dev

COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip install -r requirements.txt
RUN pip install opencv-python
RUN apt update && apt install -y libsm6 libxext6 libxrender1 libfontconfig1 libglib2.0-0

COPY . /app

ENTRYPOINT [ "python" ]

CMD [ "app.py" ]


