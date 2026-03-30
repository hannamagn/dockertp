FROM maven:3.9.9-eclipse-temurin-17

WORKDIR /app

COPY pom.xml .
COPY src ./src

RUN mvn verify

EXPOSE 8080

CMD ["java", "-Xmx64m", "-Xms64m", "-jar", "target/words.jar"]