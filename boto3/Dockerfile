FROM python:alpine
LABEL maintainer="Mihir Mone <monemihir@hotmail.com>"

ARG BOTO3_VERSION

RUN pip install boto3==${BOTO3_VERSION}

WORKDIR /root/dev

CMD ["python"]
