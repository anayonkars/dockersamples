FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update

RUN apt-get -y install tzdata

RUN apt-get -y install fortune

RUN apt-get -y install cowsay

RUN apt-get -y install lolcat

RUN apt-get -y install openjdk-8-jdk

RUN apt-get -y install openjdk-8-jre

RUN apt-get -y install maven

RUN apt-get -y install git

RUN mkdir -p /src 

RUN cd /src && git clone -v https://github.com/anayonkars/example-axon.git 

RUN cd /src/example-axon && mvn clean install

CMD /usr/games/fortune | /usr/games/cowsay | /usr/games/lolcat && cd /src/example-axon/account-domain && mvn spring-boot:run
