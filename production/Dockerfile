FROM alpine:3.16
WORKDIR /opt
RUN apk update && apk add openjdk8-jre-base
RUN wget https://dlcdn.apache.org/tomcat/tomcat-10/v10.0.23/bin/apache-tomcat-10.0.23.tar.gz && \
	tar -xvzf apache-tomcat-10.0.23.tar.gz && \
	rm apache-tomcat-10.0.23.tar.gz
#COPY hello-1.0.war apache-tomcat-10.0.23/webapps
RUN cp /tmp/app/hello-1.0.war /opt/apache-tomcat-10.0.23/webapps
RUN cp -R /tmp/app/hello-1.0 /opt/apache-tomcat-10.0.23/webapps
EXPOSE 8080
CMD ["/opt/apache-tomcat-10.0.23/bin/catalina.sh", "run"]