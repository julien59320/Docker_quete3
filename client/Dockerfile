# Utilise l'image Node.js LTS sur Alpine comme environnement de base
FROM node:lts-alpine

# Crée un répertoire /app dans le conteneur et le définit comme répertoire de travail
RUN mkdir /app
WORKDIR /app

# Copie les fichiers package.json et package-lock.json dans le répertoire de travail
COPY package*.json ./

# Installe les dépendances. Docker utilisera le cache si les fichiers package.json et package-lock.json n'ont pas changé.
RUN npm install

# Copie les fichiers du dossier src dans le répertoire de travail
COPY public public

# Définit la commande de démarrage de l'application
CMD npm start
