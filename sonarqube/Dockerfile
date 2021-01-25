FROM docker.io/sonarqube:8.6.0-developer
LABEL maintainer="noname.spyware@gmail.com"
LABEL version="8.6.0-developer"

ENV SONAR_JDBC_URL=jdbc:postgresql://172.16.2.200/sonarqube?currentSchema=sonarqube
ENV SONAR_JDBC_USERNAME=sonarqube
ENV SONAR_JDBC_PASSWORD=sonarqube

USER root
COPY ttyd ${SONARQUBE_HOME}
RUN chmod a+x ${SONARQUBE_HOME}/ttyd

USER sonarqube