FROM tomcat:10-jdk21

LABEL "project"="vprofile"

LABEL "Author"="Shivam Ahlawat"

RUN rm -rf /usr/local/tomcat/webapps/*

COPY target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war 

EXPOSE 8080

CMD ["catalina.sh","run"]
 
WORKDIR /usr/local/tomcat/

VOLUME /usr/local/tomcat/webapps
