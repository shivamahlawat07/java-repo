FROM maven:3.9.9-eclipse-temurin-21-jammy AS BUILD_IMAGE

RUN git clone https://github.com/rersharma/Adanace_Java_Project_using_vagrant_machines.git

RUN cd Adanace_Java_Project_using_vagrant_machines && git checkout docker && mvn install

FROM tomcat:10-jdk21

RUN rm -rf /usr/local/tomcat/webapps/*

COPY --from=BUILD_NAME Adanace_Java_Project_using_vagrant_machines/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080

CMD ["catalina.sh","run"]