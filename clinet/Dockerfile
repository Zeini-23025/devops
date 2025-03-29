# Utiliser une image de base Node.js
FROM node:16

# Définir le répertoire de travail
WORKDIR /app

# Copier package.json et package-lock.json
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier le reste du code source
COPY . .

# Construire l'application React
RUN npm run build

# Servir l'application React (vous pouvez utiliser un serveur comme serve)
RUN npm install -g serve
CMD ["serve", "-s", "build", "-l", "5000"]

# Exposer le port
EXPOSE 5000
