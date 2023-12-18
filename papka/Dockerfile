FROM ubuntu:latest

RUN apt-get update && apt-get install -y git

RUN echo "from emir!" > /emir.txt

RUN git config --global user.email "emir2284@yandex.ru"
RUN git config --global user.name "Emir-ooops"

ARG GITHUB_TOKEN

RUN git clone https://username:${GITHUB_TOKEN}@github.com/Emir-ooops/3-lab.git /repo
RUN cp /emir.txt /repo
WORKDIR /repo
RUN git add emir.txt
RUN git commit -m "Add emir.txt"
RUN git push origin main

