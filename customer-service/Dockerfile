FROM maven:3.9.9-eclipse-temurin-17
WORKDIR /app
VOLUME /tmp
COPY . .
RUN mvn clean package -Dmaven.test.skip=true && mv target/*.jar app.jar
ENTRYPOINT [ "java", "-jar", "app.jar" ]