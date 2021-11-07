# FROM adoptopenjdk/openjdk8
# ENV PORT 8080
# COPY target/*.jar /opt/app.jar
# WORKDIR /opt
# ENTRYPOINT exec java $JAVA_OPTS -jar app.jar


FROM adoptopenjdk/openjdk8

ENTRYPOINT ["/usr/bin/java", "-jar", "/usr/share/myservice/myservice.jar"]

# Add Maven dependencies (not shaded into the artifact; Docker-cached)
# ADD target/lib           /usr/share/myservice/lib
# Add the service itself
ARG JAR_FILE
ADD target/${JAR_FILE} /usr/share/myservice/myservice.jar