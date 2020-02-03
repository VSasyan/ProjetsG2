# ProjetsG2

## Installation de Postgres Ubuntu

#### Installation système

```sh
sudo apt update
sudo apt install postgresql postgresql-contrib postgis
```

#### Configuration

Authorisation de se connecter via mot de passe (pour pouvoir accéder à la base depuis PgAdmin, Python, etc) :

```sh
# On passe en utilisation postgres
sudo su postgres
# On se connecte à la base
psql
```

On ajoute à l'utilisateur la possibilité de se connecter via mdp :

```sql
ALTER USER postgres WITH PASSWORD 'postgres';
```

Quitter la connexion SQL et la session `postgres` :

```
Ctrl+D
Ctrl+D
```
#### Exension géographiques

Il faut ajouter l'extension géographique à votre base de données :

```sql
CREATE EXTENSION postgis;
```

Ceci est un code SQL à lancer en étant connecté à la base.
