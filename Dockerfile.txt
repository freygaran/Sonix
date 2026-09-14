# 1. Utiliser l'image Java officielle (ici Java 17, changez par 21 ou 11 si besoin)
FROM eclipse-temurin:17-jdk-alpine

# 2. Définir le dossier de travail interne
WORKDIR /app

# 3. Copier votre JAR dans le conteneur en le renommant plus simplement
COPY Sonix-0.0.1-SNAPSHOT.jar app.jar

# 4. Indiquer le port (généralement 8080 pour du Spring Boot)
EXPOSE 8080

# 5. Commande pour exécuter votre application
ENTRYPOINT ["java", "-jar", "app.jar"]
