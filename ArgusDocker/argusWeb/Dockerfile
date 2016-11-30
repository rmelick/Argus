FROM node:7.2.0

RUN apt-get update -y && apt-get install -y telnet net-tools
RUN npm install -g bower
RUN npm install -g grunt

COPY ArgusWeb /usr/argus/argusWeb
WORKDIR /usr/argus/argusWeb
RUN npm install && bower --allow-root install && grunt

EXPOSE 8000
CMD ["npm", "start"]

