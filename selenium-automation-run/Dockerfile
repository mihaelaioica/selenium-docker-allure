FROM blazemeter/selenium_base:latest

# create project folder with the name code
RUN mkdir /code

# project scope
WORKDIR /code

# pip
COPY blazedemo_app/requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt
RUN easy_install -U setuptools
RUN pip install pytest-dependency

# Dokcer entry
COPY blazedemo_app/docker-entry.sh /code
ENTRYPOINT ["/docker-entry.sh"]

CMD ["/bin/true"]
