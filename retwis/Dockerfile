# docker build -t retwis:latest .

FROM python:3.7-alpine

# Install the flask python dependencies via pip
RUN mkdir -p /retwis/reqs 
COPY ./reqs/requirements.txt /retwis/reqs/requirements.txt
RUN pip install -r retwis/reqs/requirements.txt

# Install retwis
RUN mkdir -p  /retwis/templates
COPY ./templates/layout.html /retwis/templates/layout.html
COPY ./templates/login.html /retwis/templates/login.html
COPY ./templates/signup.html /retwis/templates/signup.html
COPY ./templates/home.html /retwis/templates/home.html
RUN mkdir -p /retwis/static
COPY ./static/style.css /retwis/static/style.css
COPY ./views.py /retwis/views.py
COPY ./settings.py /retwis/settings.py
COPY ./runserver.py /runserver.py
COPY ./__init__.py /retwis/__init__.py

# Start retwis
CMD python runserver.py
