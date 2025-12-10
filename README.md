# Déploiement Wordpress + MariaDB + Nginx avec Docker Compose

Cette procédure permet de déployer un environnement complet WordPress sur Debian à l’aide de Docker, regroupant :
- MariaDB (base de données)
- WordPress en PHP-FPM
- Nginx (reverse proxy)

---

## 1. Installation des dépendances

```bash
apt install docker.io -y
apt install docker-compose -y

## 2. Préparation de l’arborescence
mkdir -p /etc/my_wordpress/nginx
mkdir -p /etc/my_wordpress/wordpress
cd /etc/my_wordpress/

## 3. Fichier d’environnement (.env)

Créer le fichier :

nano .env


Contenu :

MYSQL_ROOT_PASSWORD=SuperRootPassword
MYSQL_DATABASE=wordpress
MYSQL_USER=wpuser
MYSQL_PASSWORD=WpUserPassword