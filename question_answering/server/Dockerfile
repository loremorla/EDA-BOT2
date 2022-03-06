From ubuntu:latest

WORKDIR /src

RUN apt-get update && apt-get install python3-pip python3 -y && apt-get install wget -y && apt-get install zip -y

RUN mkdir /app

RUN mkdir -p /src/model

RUN wget https://public.ukp.informatik.tu-darmstadt.de/reimers/sentence-transformers/v0.2/paraphrase-mpnet-base-v2.zip

RUN unzip paraphrase-mpnet-base-v2.zip -d /src/model/paraphrase-mpnet-base-v2/

RUN pip3 install -r /app/requirements.txt -i https://mirrors.aliyun.com/pypi/simple --trusted-host mirrors.aliyun.com

CMD python3 main.py
