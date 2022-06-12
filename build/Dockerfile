FROM alpine:latest
RUN apk add --update git maven openjdk8
WORKDIR /data
RUN git clone https://github.com/daticahealth/java-tomcat-maven-example    
WORKDIR /data/java-tomcat-maven-example
RUN mvn package
WORKDIR /share
CMD mv /data/java-tomcat-maven-example/target/java-tomcat-maven-example.war ./ROOT.war
