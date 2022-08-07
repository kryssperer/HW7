FROM ubuntu:20.04
RUN apt update
RUN apt install default-jdk -y && apt install maven -y && apt install tree -y
WORKDIR /tmp/app
COPY pom.xml .
COPY src .
WORKDIR /opt/app
RUN pwd
RUN mvn clean package --file /tmp/app/pom.xml && cp /tmp/app/target/hello-1.0.war /opt/app
