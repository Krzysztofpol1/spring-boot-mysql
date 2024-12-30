FROM ubuntu
RUN apt-get update -y
RUN apt-get install -y openjdk-11-jdk
RUN mkdir /opt/tomcat
WORKDIR /opt/tomcat
ADD https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.54/bin/apache-tomcat-9.0.54.tar.gz /opt/tomcat
RUN apt install -y tar gzip wget
RUN tar -xvzf apache-tomcat-9.0.54.tar.gz
RUN mv apache-tomcat-9.0.54/* /opt/tomcat
EXPOSE 8080
COPY target/spring-boot-faces-first-no-ldap-app.war /opt/tomcat/webapps
CMD ["/opt/tomcat/bin/catalina.sh","run"]
