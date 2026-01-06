# Dockerfile

# Author       : adhikarisubodh9991
# Github       : https://github.com/adhikarisubodh9991
# Date         : 25-08-2021
# Main Language: Python

# Download and import main images

# Operating system
FROM debian:latest
# Main package
FROM python:3

# Author info
LABEL MAINTAINER="https://github.com/adhikarisubodh9991/PyPhisher"

# Working directory
WORKDIR PyPhisher/
# Add files 
ADD . /PyPhisher

# Installing other packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install php openssh-client -y
RUN pip3 install -r files/requirements.txt
RUN apt-get clean

# Main command
CMD ["python3", "pyphisher.py", "--noupdate"]

## Wanna run it own? Try following commnads:

## "sudo docker build . -t adhikarisubodh9991/pyphisher:latest", "sudo docker run --rm -it adhikarisubodh9991/pyphisher:latest"

## "sudo docker pull adhikarisubodh9991/pyphisher", "sudo docker run --rm -it adhikarisubodh9991/pyphisher"
