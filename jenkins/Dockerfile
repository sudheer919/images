#rkalluru/k04-jenkins:v1
FROM jenkins/jenkins:lts-alpine 
USER root 
RUN apk add docker 
RUN apk add git 
RUN addgroup jenkins root 
COPY make-docker-image /bin 
RUN chmod +x /bin/make-docker-image 
USER jenkins