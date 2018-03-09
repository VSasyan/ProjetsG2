# ProjetsG2

## Installation de Postgres Ubuntu

#### Installation système

```
sudo apt update
sudo apt install postgresql postgresql-contrib
```

#### Configuration

Authorisation de se connecter via mot de passe (pour pouvoir accéder à la base depuis PgAdmin, Python, etc) :

```
# On passe en utilisation postgres
sudo su postgres
# On se connecte à la base
psql
```

On ajoute à l'utilisateur la possibilité de se connecter via mdp :

```
ALTER USER postgres WITH PASSWORD 'postgres';
```

Quitter la connexion SQL et la session `postgres` :

```
Ctrl+D
Ctrl+D
```
