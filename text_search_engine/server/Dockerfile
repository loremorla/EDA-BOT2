From ubuntu:latest

WORKDIR /src

RUN apt-get update && apt-get install python3-pip python3 -y && apt-get install wget -y && apt-get install zip -y

RUN mkdir -p /src/model

RUN wget https://public.ukp.informatik.tu-darmstadt.de/reimers/sentence-transformers/v0.2/paraphrase-mpnet-base-v2.zip

RUN unzip paraphrase-mpnet-base-v2.zip -d /src/model/paraphrase-mpnet-base-v2/

RUN pip3 --default-timeout=1000 install -r requirements.txt 

CMD python3 main.py