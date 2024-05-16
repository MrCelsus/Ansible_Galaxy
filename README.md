# Ansible_Galaxy

Pour automatiser l'installation de PHPMyAdmin et la configuration de MariaDB en utilisant Ansible, nous allons créer deux rôles distincts : phpmyadmin et database. Chaque rôle sera organisé avec la structure typique d'un rôle Ansible (defaults, handlers, tasks, etc.). Ensuite, nous écrirons un playbook principal deploy_pma.yml qui utilisera ces deux rôles.

Voici les étapes suivantes :

## Création des répertoires des rôles :

Les roles doivent être créer dans un environnement Ansible
`mkdir -p roles/phpmyadmin/{tasks,defaults,handlers,templates,files,vars}
mkdir -p roles/database/{tasks,defaults,handlers,templates,files,vars}`

## Configuration du role 'database' :

Vous retrouverez tous les fichiers de configuration dans les dossiers nécessaires.

## Configuration du role 'phpmyadmin' :

Vous retrouverez tous les fichiers de configuration dans les dossiers nécessaires.

## Création du playbook principal 'deploy_pma' :

Création du playbook à la racine du projet afin de pouvoir le lancer.

## Création du inventory.ini

Un fichier est dédié pour ajouter vos machines

## Lancement du playbook :

Utilisez la commande suivante pour exécuter le playbook :
`ansible-playbook -i inventory.ini deploy_pma.yml`

# Remarque

Cette structure permet de séparer les configurations spécifiques à MariaDB et PHPMyAdmin en rôles distincts, tout en les unissant via un playbook principal pour une gestion et une maintenance facilitées. N'oubliez pas d'adapter les configurations aux spécificités de votre environnement, notamment les fichiers de configuration et les paramètres de sécurité.
