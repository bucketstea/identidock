FROM python:3.9

RUN pip install --upgrade pip \
    && pip install Flask uWSGI requests redis \
    && groupadd -r uwsgi && useradd -r -g uwsgi uwsgi

WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]

