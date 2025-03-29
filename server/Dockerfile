# Utilisation de l'image officielle OpenJDK
FROM maven:3.8.4-openjdk-17-slim AS build

# Définir le répertoire de travail dans l'image Docker
WORKDIR /app

# Copier le fichier pom.xml et télécharger les dépendances
COPY pom.xml .

# Télécharger les dépendances Maven
RUN mvn dependency:go-offline

# Copier le code source
COPY src /app/src

# Construire l'application Spring Boot et générer le fichier JAR
RUN mvn clean package -DskipTests

# Utilisation de l'image officielle OpenJDK pour l'exécution
FROM openjdk:17-jdk-slim

# Définir le répertoire de travail dans l'image Docker
WORKDIR /app

# Copier le fichier JAR généré dans le conteneur
COPY --from=build /app/target/server-0.0.1-SNAPSHOT.jar app.jar

# Exposer le port utilisé par l'application Spring Boot
EXPOSE 8080

# Lancer l'application Spring Boot
CMD ["java", "-jar", "app.jar"]
