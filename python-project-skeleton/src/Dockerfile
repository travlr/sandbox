# FROM ubuntu:latest  
# RUN apt-get update   
#     && apt-get install --no-install-recommends --no-install-suggests -y curl 
#     && rm -rf /var/lib/apt/lists/*
# ENV SITE_URL http://example.com/  
# WORKDIR /data  
# VOLUME /data  
# CMD sh -c "curl -Lk $SITE_URL > /data/results"  

# start with a base image
FROM python:3.7

# update pip
RUN python -m pip install --upgrade pip

# set working diretory
WORKDIR /code

# copy requirements.txt and install
COPY requirements.txt requirements.txt
RUN python -m pip install -r requirements.txt

# copy all project files
COPY . .

# CMD ["python", "main.py"]