FROM python:3.10-alpine
# Buffered mode means that the output will be flushed to the console immediately rather than being held in a buffer.
ENV PYTHONBUFFERED 1
WORKDIR /django
# Separating the COPY requirements.txt requirements.txt and RUN pip3 install -r requirements.txt 
# lines is a common practice in Dockerfiles to take advantage of caching and optimize the build process.
RUN pip3 install -r requirements.txt 
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt
COPY . .
