FROM tomcat:7.0.73-jre8

RUN apt-get update -y && apt-get install -y telnet net-tools

COPY ArgusWebServices/target/argus-webservices-2.2.0-SNAPSHOT.war ${CATALINA_HOME}/webapps/argus.war
ENV CATALINA_OPTS="-Dargus.config.public.location=/usr/argus/argus.properties"