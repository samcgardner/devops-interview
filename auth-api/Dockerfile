# basic Dockerfile to build all and run any Python service
FROM jfloff/alpine-python:recent-onbuild

# install dependencies
COPY requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

# run flask server
EXPOSE 5000
COPY run.py /usr/local/run.py
COPY users.json /usr/local/users.json
CMD python /usr/local/run.py
