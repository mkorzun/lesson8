FROM alpine:latest
RUN set -x \
 && apk update \
 && apk add  --no-cache --virtual .checksum-deps \
      openjdk8-jre-base \
      wget
RUN set -x \
  && mkdir /opt/tomcat \
  && wget https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.75/bin/apache-tomcat-8.5.75.tar.gz \
  && tar xvzf apache-tomcat-8.5.75.tar.gz  --strip-components 1 --directory /opt/tomcat \
  && rm -rf apache-tomcat-8.5.75.tar.gz
CMD ["/opt/tomcat/bin/catalina.sh", "run"]