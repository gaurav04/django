FROM python:3.7-alpine

WORKDIR /admin

RUN \
apk update && \
pip install virtualenv && \
apk add make && \
apk add --no-cache postgresql-dev  && \
apk add --no-cache postgresql-libs && \
apk add --no-cache --virtual .build-deps gcc musl-dev postgresql-dev

COPY . /admin

RUN make venv


EXPOSE 8000

CMD ["venv/bin/python", "manage.py","runserver", "0.0.0.0:8000"]
