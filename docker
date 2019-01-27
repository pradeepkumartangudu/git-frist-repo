FROM centos:centos7

#Install Java
RUN yum -y install java-1.8.0-openjdk-devel

#Extracting the nodejs from the source
RUN curl -sL https://rpm.nodesource.com/setup_10.x -o nodejs.sh | bash -

#Extracts required nodejs packages
RUN sh nodejs.sh

#Install node.js
RUN yum -y install nodejs

#Copy the application onto workdir
ADD Automation /opt/Automation

#Setting the workdir
WORKDIR /opt/Automation

RUN npm install -g nightwatch

#Install NPM
RUN npm install

RUN npm install --save-dev nodemon

RUN npm install express --save

RUN npm run start &