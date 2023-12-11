# Stage de construction
FROM maven:3.8.2-jdk-11 AS build
WORKDIR /app
COPY . .
RUN mvn clean package -Pprod -DskipTests

# Stage de package
FROM openjdk:11
WORKDIR /app
COPY --from=build /app/target/Notes-0.0.1-SNAPSHOT.jar Notes.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "Notes.jar"]
