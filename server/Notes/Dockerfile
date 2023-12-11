# Stage de construction
FROM maven:3.8.2-openjdk-17 AS build
WORKDIR /app
COPY . .
RUN mvn clean package -Pprod -DskipTests

# Stage de package
FROM openjdk:17
WORKDIR /app
COPY --from=build /app/target/Notes-0.0.1-SNAPSHOT.jar Notes.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "Notes.jar"]

