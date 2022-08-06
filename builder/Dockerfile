FROM ubuntu:20.04
RUN apt update
RUN apt install default-jdk -y && apt install maven -y
WORKDIR /tmp/app
#COPY pom.xml .
#COPY src .
RUN pwd
RUN ls -R
RUN mvn clean package
RUN cp /tmp/app/target/hello-1.0.war /tmp/app