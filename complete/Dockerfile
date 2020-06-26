FROM openjdk:8-jdk-alpine
USER root
RUN mkdir /app
RUN addgroup -S spring && adduser -S spring -G spring
USER spring:spring
ARG DEPENDENCY=target/dependency
COPY target/*.jar /app/app.jar
WORKDIR /app
ENTRYPOINT ["java","-jar", "app.jar"]
