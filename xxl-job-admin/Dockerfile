FROM openjdk:8-jre-slim
MAINTAINER xuxueli

ENV PARAMS=""

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ADD target/xxl-job-admin-*.jar /app.jar

EXPOSE 8082

ENTRYPOINT ["sh","-c","java -jar $JAVA_OPTS /app.jar $PARAMS"]
