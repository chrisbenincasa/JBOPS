FROM python:3-alpine3.18

ENV PLEX_URL=127.0.0.1:32000
ENV PLEX_TOKEN=token

RUN mkdir -p /usr/local/jbpos
WORKDIR /usr/local/jbops

COPY requirements.txt /usr/local/jbops/requirements.txt
RUN pip install --upgrade pip && pip install -r /usr/local/jbops/requirements.txt

ADD fun /usr/local/jbops/fun
ADD killstream /usr/local/jbops/killstream
ADD maps /usr/local/jbops/maps
ADD notify /usr/local/jbops/notify
ADD reporting /usr/local/jbops/reporting
ADD utility /usr/local/jbops/utility

COPY config.ini /usr/local/jbops/config.ini

ENTRYPOINT ["/bin/sh"]
