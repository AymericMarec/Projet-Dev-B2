# 🍽️ Customer Service - Projet Dev

## 📋 Vue d'ensemble du Projet
Ce projet est un système complet de gestion de restaurant composé de quatre applications interconnectées qui optimisent le processus de commande et de service dans un restaurant. Le système comprend une application client pour les clients, un système d'affichage pour la cuisine, une application mobile pour les serveurs et une API centrale.

## 🏗️ Architecture du Système

### 1. Application Client (Tablette) 📱
- **Repository**: [CustomerService-Client](https://github.com/AymericMarec/CustomersService-Client)
- **Description**: Une application basée sur Electron pour les tablettes placées sur les tables du restaurant, permettant aux clients de parcourir le menu et de passer leurs commandes directement.
- **Technologies**: Electron, JavaScript

### 2. Système d'Affichage Cuisine 👨‍🍳
- **Repository**: [CustomerServices-Kitchen](https://github.com/AymericMarec/CustomerServices-Kitchen)
- **Description**: Une interface dédiée pour le personnel de cuisine pour visualiser et gérer les commandes entrantes. Les commandes sont affichées dans une file d'attente prioritaire, et le personnel de cuisine peut marquer les commandes comme terminées.
- **Technologies**: Electron, JavaScript

### 3. Application Mobile Serveur 👨‍💼
- **Repository**: [CustomerService-Waiter](https://github.com/AymericMarec/CustomersService-Waiter)
- **Description**: Une application mobile pour les serveurs qui leur permet de recevoir uniquement les commandes qui leur sont assignées. L'API gère automatiquement la distribution des commandes aux serveurs disponibles.
- **Technologies**: React Native, TypeScript

### 4. API Backend 🔧
- **Repository**: [CustomersService-API](https://github.com/AymericMarec/CustomersService-API)
- **Description**: L'API centrale qui gère tout le flux de données entre les différentes applications, traite les commandes et maintient la base de données. Elle gère également la distribution intelligente des commandes aux serveurs disponibles.Elle possède aussi une partie administrateur pour créer gérer le menu du restaurant
- **Technologies**: Symfony, PHP, MySQL

## 🚀 Installation et Configuration

### Prérequis
- Node.js (v14 ou supérieur)
- PHP 8.1 ou supérieur
- Composer
- MySQL
- Git
- Make

### Configuration de l'API Backend
1. Cloner le repository de l'API :
```bash
git clone https://github.com/AymericMarec/CustomersService-API.git
cd CustomersService-API
```

3. Créer le fichier .env.local :
```bash
# Créer le fichier .env.local à la racine du projet
```

Ajouter les configurations suivantes dans le fichier .env.local :
```env
DATABASE_URL=mysql://symfony:symfony@127.0.0.1:3306/CustomersService
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=CustomersService
MYSQL_USER=symfony
MYSQL_PASSWORD=symfony
```

4. Pour initialiser le projet :

Un choix va vous etre proposé , ecrivez "yes"

```bash
make init
```

5. Pour démarrer l'api :
```bash
make start
```

### Configuration de l'Application Client
1. Cloner le repository client :
```bash
git clone https://github.com/AymericMarec/CustomerService-Client.git
cd CustomerService-Client
```

2. Installer les dépendances :
```bash
npm install
```

3. Créer le fichier .env :
```bash
# Créer le fichier .env à la racine du projet
```

Ajouter les configurations suivantes :
```env
API_URL=http://IP:8000
TABLE_ID=1  # À modifier selon la table où l'application est installée
```

4. Démarrer l'application :
```bash
npm start
```

### Configuration du Système d'Affichage Cuisine
1. Cloner le repository cuisine :
```bash
git clone https://github.com/AymericMarec/CustomerServices-Kitchen.git
cd CustomerServices-Kitchen
```

2. Installer les dépendances :
```bash
npm install
```

3. Créer le fichier .env :
```bash
# Créer le fichier .env à la racine du projet
```

Ajouter la configuration suivante :
```env
API_URL=http://IP:8000
```

4. Démarrer l'application :
```bash
npm start
```

### Configuration de l'Application Mobile Serveur
1. Cloner le repository serveur :
```bash
git clone https://github.com/AymericMarec/CustomerService-Waiter.git
cd CustomerService-Waiter
```

2. Installer les dépendances :
```bash
npm install
```

3. Créer le fichier .env :
```bash
# Créer le fichier .env à la racine du projet
```

Ajouter la configuration suivante :
```env
API_URL=http://IP:8000
```

4. Démarrer l'application :
```bash
npm start
```

Pour l'application serveur , vous pouvez , installer l'application expo Go puis scanner le QR code du terminal , pensez a bien changer l'ip dans le .env , en mettant l'ip en local de l'api et non localhost

Vous pouvez aussi visitez http://localhost:8081/ReadyCommand pour avoir la version web

## 🔄 Flux de Travail
1. Les clients passent leurs commandes via l'application tablette
2. Les commandes sont automatiquement envoyées au système d'affichage cuisine
3. Le personnel de cuisine prépare les commandes et les marque comme terminées
4. L'API assigne automatiquement les commandes terminées aux serveurs disponibles
5. Les serveurs reçoivent uniquement les notifications des commandes qui leur sont assignées
6. Les serveurs servent les commandes et les marquent comme servies dans leur application
7. Les commandes sont supprimées du système une fois servies

## ✨ Fonctionnalités
- Gestion des commandes en temps réel
- Distribution automatique des commandes aux serveurs
- Notifications push pour les commandes terminées
- Système de gestion des tables
- Suivi du statut des commandes
- Design responsive pour toutes les applications
- Points d'accès API sécurisés
- Persistance des données

## Contacts

En cas de problème veuillez contacter une des personnes suivantes via discord :

@yvel__
@dianesdp
@linuxo
@mafraisefr2
