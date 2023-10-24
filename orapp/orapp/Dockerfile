FROM openjdk:8

ENV TZ=Asia/Shanghai

EXPOSE 8000

RUN ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime \
&& echo $TIME_ZONE > /etc/timezone

COPY *.jar /opt/app.jar

ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom" ,"-jar","/opt/app.jar"]
