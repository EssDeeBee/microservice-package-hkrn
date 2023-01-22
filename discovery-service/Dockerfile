FROM bellsoft/liberica-openjdk-alpine-musl
COPY ./target/discovery-service-0.0.1-SNAPSHOT.jar /usr/app/
WORKDIR /usr/app
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "discovery-service-0.0.1-SNAPSHOT.jar"]