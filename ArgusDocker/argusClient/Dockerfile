FROM openjdk:8u111-jre

RUN apt-get update -y && apt-get install -y telnet net-tools less vim

RUN mkdir -p /usr/argus/argusClient
COPY ArgusClient/client.sh /usr/argus/argusClient/
COPY ArgusClient/README.md /usr/argus/argusClient/
COPY ArgusClient/src/main/resources/com/salesforce/dva/argus/client/usage.txt /usr/argus/argusClient/

WORKDIR /usr/argus/argusClient

ENTRYPOINT ["./client.sh"]
