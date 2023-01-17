# Prérequis :
-Abonnenement Azure
-Visual Studio Code
-Git
-Docker Destop 
-Extension Docker pour Visual Studio Code

#Initialiser le projet
Cloner le dépôt suivant avec Visual Studio Code : https://github.com/hinault/azure-container

Ouvrir le projet dans Visual Studio Code.

Ajouter un nouveau fichier Dockerfile dans le répertoire app avec le contenu suivant :

```
# syntax=docker/dockerfile:1
FROM node:18-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
```


# Générer l’image 

Faire un clic droit sur le fichier Dockerfile puis cliquer sur Build pour générer l’image de conteneur. 

Utiliser l’extension Docker de VS Code pour exécuter et tester l’image

#Publier dans Azure Container Registry

Créer un registre de conteneur à partir du portail Azure.

Activer le compte administrateur.

Utiliser l’extension Docker de VS Code pour pousser l’image dans ACR.

