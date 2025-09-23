# Use Eclipse Temurin JRE 17 on Alpine (lightweight image)
FROM eclipse-temurin:17-jre-alpine

# Path to the Spring Boot jar (built by Maven/Gradle)
ARG artifact=target/spring-boot-web.jar

# Set working directory inside container
WORKDIR /opt/app

# Copy the jar file into the container
COPY ${artifact} app.jar

# Expose the app port (default for Spring Boot)
EXPOSE 8080

# Start the Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]
