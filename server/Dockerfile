# Utilisation de l'image officielle OpenJDK
FROM openjdk:17-jdk-slim

# Définir le répertoire de travail dans l'image Docker
WORKDIR /app

# Copier le fichier JAR généré dans le conteneur
COPY target/server-0.0.1-SNAPSHOT.jar app.jar

# Exposer le port utilisé par l'application Spring Boot
EXPOSE 8080

# Lancer l'application Spring Boot
CMD ["java", "-jar", "app.jar"]
