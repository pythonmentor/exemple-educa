# Exemple d'application Django

Cet exemple d'application Django est tirée de l'ouvrage "Django 4 by example" de Antonio Mele chez Packt Publishing. Le code cours original de l'application [se trouve sur ce repo](https://github.com/PacktPublishing/Django-4-by-example/tree/main/Chapter15). 

L'application dans le présent dépôt de code a été légèrement modifiée pour un cours sur le déploiement
d'application Django. 

## Dépendance

Cette application de démonstration a besoin de redis pour fonctionner. Le fichier docker-compose.yml disponible
à la racine du projet est là pour vous faciliter la vie. Il fait tourner une instance de Redis sur le
port 6379 de votre ordinateur. Il fait également tourner une instance de MariaDB version 10.6.16 sur le port 23306, une instance de MySQL (version la plus récente) sur le port 33306, et une instance de PostgreSQL (version la plus récente) sur le port 25432.

Les données de connexion à la base de données sont:

- Utilisateur: educa
- Mot de passe: educa
- Nom de la base de données: educa

## Prise en main de l'exemple

Pour tester cette application, suivre les indications suivantes:

1. Démarrer les serveurs de base de données avec `docker compose up -d`
1. Créer un répertoire .venv vide et installer les dépendance à l'aide de pipenv avec `pipenv install`
1. Activer l'environnement virtuel avec `pipenv shell`
1. Exécuter les migrations avec `python manage.py migrate`
1. Installer les données de démarrage avec `python manage.py loaddata data`

Un **superutilisateur** a été crée pour vous. Son username est admin et son mot de passe est educa.