FROM openjdk:8-jdk-alpine
RUN addgroup -S spring && adduser -S spring -G spring
USER spring:spring
ARG DEPENDENCY=target/dependency
RUN mkdir /app
COPY target/*.jar /app/app.jar
WORKDIR /app
ENTRYPOINT ["java","-jar", "app.jar"]
