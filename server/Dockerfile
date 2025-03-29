# Utiliser une image de base Java
FROM openjdk:17-jdk-slim

# Copier le fichier JAR généré par Spring Boot
COPY target/*.jar app.jar

# Exposer le port que l'application utilise
EXPOSE 8080

# Commande pour lancer l'application
ENTRYPOINT ["java", "-jar", "/app.jar"]
