FROM openjdk:8-jdk-alpine

ARG PORT=8080
ARG DEPENDENCY=target/dependency

EXPOSE $PORT

WORKDIR /tmp
RUN mkdir -p app
COPY ${DEPENDENCY}/BOOT-INF/lib app/lib
COPY ${DEPENDENCY}/META-INF app/META-INF
COPY ${DEPENDENCY}/BOOT-INF/classes app/

ENTRYPOINT ["java", "-cp", "app:app/lib/*","com.in28minutes.rest.webservices.restfulwebservices.RestfulWebServicesApplication"]