# BobApp

[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=Aleod-m_Gerez-un-projet-collaboratif-en-int-grant-une-demarche-CI-CD&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=Aleod-m_Gerez-un-projet-collaboratif-en-int-grant-une-demarche-CI-CD)

[![TEST](https://github.com/Aleod-m/Gerez-un-projet-collaboratif-en-int-grant-une-demarche-CI-CD/actions/workflows/test.yml/badge.svg)](https://github.com/Aleod-m/Gerez-un-projet-collaboratif-en-int-grant-une-demarche-CI-CD/actions/workflows/test.yml)

Clone project:

> git clone XXXXX

## Front-end 

Go inside folder the front folder:

> cd front

Install dependencies:

> npm install

Launch Front-end:

> npm run start;

### Docker

Build the container:

> docker build -t bobapp-front .  

Start the container:

> docker run -p 8080:8080 --name bobapp-front -d bobapp-front

## Back-end

Go inside folder the back folder:

> cd back

Install dependencies:

> mvn clean install

Launch Back-end:

>  mvn spring-boot:run

Launch the tests:

> mvn clean install

### Docker

Build the container:

> docker build -t bobapp-back .  

Start the container:

> docker run -p 8080:8080 --name bobapp-back -d bobapp-back 
