FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl
RUN apt-get install -y git
RUN git clone https://github.com/docker-hy/frontend-example-docker 1.10/

WORKDIR /1.10

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN npm install

EXPOSE 5000

ENTRYPOINT API_URL=http://localhost:8888 npm start
