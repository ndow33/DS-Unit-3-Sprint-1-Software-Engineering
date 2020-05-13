FROM debian

### So logging/io works reliably w/Docker
ENV PYTHONUNBUFFERED=1
### UTF Python issue for Click package (pipenv dependency)
ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8
### Need to explicitly set this so `pipenv shell` works
ENV SHELL=/bin/bash
ENV SECRET_MESSAGE="Hello world :-D"

### Basic Python dev dependencies
RUN apt-get update && \
  apt-get upgrade -y && \
  apt-get install python3-pip curl -y && \
  pip3 install pipenv

RUN pip3 install pandas
RUN pip3 install -i https://test.pypi.org/simple/ my-lambdata-ndow33==1.2