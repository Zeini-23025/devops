# Utilisation de l'image officielle Node.js
FROM node:18

# Définir le répertoire de travail dans l'image Docker
WORKDIR /app

# Copier les fichiers package.json et package-lock.json
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier le reste des fichiers du projet
COPY . .

# Construire l'application React
RUN npm run build

# Exposer le port (si nécessaire)
EXPOSE 3000

# Lancer l'application React avec un serveur comme 'serve'
CMD ["npm", "run", "preview"]
