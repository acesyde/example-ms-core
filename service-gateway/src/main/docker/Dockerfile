FROM frolvlad/alpine-oraclejdk8:slim
VOLUME /tmp
ADD service-gateway-0.1.0.jar app.jar
RUN sh -c 'touch /app.jar'
ENV JAVA_OPTS="-Xmx200m"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]