FROM python:3.6.0-alpine

WORKDIR /app
ADD . /app

# RUN apk --no-cache --update add build-base=0.4-r1 && \
#     pip install -r /app/requirements.txt --trusted-host pypi.python.org && \
#     apk del build-base
RUN apk --no-cache --update add build-base gcc musl-dev && \
    pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host files.pythonhosted.org --upgrade pip && \
    pip install -r /app/requirements.txt && \
    apk del build-base

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

ENTRYPOINT ["python3", "post_app.py"]
