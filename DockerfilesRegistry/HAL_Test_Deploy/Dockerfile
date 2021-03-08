FROM ubuntu:bionic

RUN apt-get update && \

        apt-get install -y build-essential git wget software-properties-common python3.7

RUN apt install -y python-pip

RUN pip install robotframework

RUN pip install robotframework-scplibrary

RUN add-apt-repository ppa:openjdk-r/ppa

RUN apt -y install openjdk-14-jdk

RUN export JAVA_HOME=/usr/lib/jvm/openjdk-14-jdk

RUN export PATH=$PATH:$JAVA_HOME/bin

RUN java -version

WORKDIR /src/Deploy

CMD robot .
