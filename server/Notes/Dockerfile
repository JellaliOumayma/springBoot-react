# Utilisation d'une image de base Java
FROM openjdk:16

# Répertoire de travail
WORKDIR /app

# Copier le fichier JAR de l'application Spring Boot dans le conteneur
COPY target/Notes-0.0.1-SNAPSHOT.jar /app/ Notes.jar


# Exposer le port sur lequel l'application Spring Boot fonctionne (par exemple, 8080)
EXPOSE 8080

# Commande pour lancer l'application Spring Boot
CMD ["java", "-jar", "Notes.jar"]


