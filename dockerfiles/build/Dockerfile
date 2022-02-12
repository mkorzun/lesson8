FROM maven:3.8.4-jdk-8 AS build
RUN set -x \
  && git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git /tmp/boxfuse-sample-java-war-hello-war-hello \
  && mvn -f /tmp/boxfuse-sample-java-war-hello-war-hello/pom.xml clean package \
  && mv /tmp/boxfuse-sample-java-war-hello-war-hello/target/hello-*.war /data