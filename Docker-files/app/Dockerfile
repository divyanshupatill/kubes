# vProfile App Dockerfile - Tomcat 10 with JDK 21
FROM tomcat:10-jdk21
LABEL "Project"="Vprofile"
LABEL "Author"="Divyanshu"

RUN rm -rf /usr/local/tomcat/webapps/*
COPY target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

WORKDIR /usr/local/tomcat/
EXPOSE 8080
VOLUME /usr/local/tomcat/webapps

HEALTHCHECK --interval=30s --timeout=5s --retries=3 \
  CMD curl -f http://localhost:8080/ || exit 1

CMD ["catalina.sh", "run"]
