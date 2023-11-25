# Apache SQL PHP stack


This is a docker compose image project.

It provides a way to have an Apache server with PHP support and connection to an SQL database
server. The database server is choosen between MariaDB, MySQL or PostgreSQL.


## What's inside ?

The compose file builds a php 8.1 image with apache server. Composer and Symfony are added in.

To manage the DB server the adminer image is built too.

I let you read the `docker/docker-compose.yml` file.


## How it works ?

The DB server choice is actually made using the `--profile` option on command line.

You'll have to choose between these profiles:

+ mariadb
+ mysql
+ pgsql

The `app` directory is where you'll have to put your web files.


---


Il s'agit d'un projet d'image Docker Compose.

Il offre la possibilité d'avoir un serveur Apache avec prise en charge de PHP et une connexion à un serveur de base de données SQL. Le choix du serveur de base de données se fait entre MariaDB, MySQL ou PostgreSQL.


## Que contient-il ?

Le fichier de composition construit une image php 8.1 avec un serveur Apache. Composer et Symfony y sont ajoutés.

Pour gérer le serveur de base de données, l'image d'adminer est également construite.

Je vous laisse consulter le fichier `docker/docker-compose.yml`.


## Comment cela fonctionne-t-il ?

Le choix du serveur de base de données se fait réellement en utilisant l'option `--profile` en ligne de commande.

Vous devrez choisir entre ces profils :

+ mariadb
+ mysql
+ pgsql

Le répertoire `app` est l'endroit où vous devrez placer vos fichiers web.

