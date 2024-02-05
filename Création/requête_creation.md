# Les différentes requêtes pour créer la base de données

## Requête pour créer la base de données :
```sql
CREATE DATABASE IF NOT EXISTS Streaming
```

## Requêtes pour créer les tables :
### Pour créer la table films :
```sql
CREATE TABLE films (
id_films int NOT NULL PRIMARY KEY AUTO_INCREMENT,
titre_films varchar(255) NOT NULL,
date_sortie_films DATE NOT NULL,
id_realisateurs int NOT NULL,
duree_films TIME NOT NULL,
CONSTRAINT FK_films_realisateurs
FOREIGN KEY (id_realisateurs)
REFERENCES realisateurs(id_realisateurs)
)
```

### Pour créer la table réalisateurs :
```sql
CREATE TABLE realisateurs (
id_realisateurs int NOT NULL PRIMARY KEY AUTO_INCREMENT,
nom_realisateurs varchar(255) NOT NULL,
prenom_realisateurs varchar(255) NOT NULL,
date_naissance_realisateurs DATE NOT NULL
)
```

### Pour créer la table utilisateurs :
```sql
CREATE TABLE utilisateurs (
id_utilisateurs int NOT NULL PRIMARY KEY AUTO_INCREMENT,
nom_utilisateurs varchar(255) NOT NULL,
prenom_utilisateurs varchar(255) NOT NULL,
date_naissance_utilisateurs DATE NOT NULL,
adresse_mail_utilisateurs varchar(255) NOT NULL,
mot_de_passe_utilisateurs varchar(255) NOT NULL,
role_utilisateurs varchar(255) NOT NULL,
)
```

### Pour créer la table acteurs :
```sql
CREATE TABLE acteurs (
id_acteurs int NOT NULL PRIMARY KEY AUTO_INCREMENT,
nom_acteurs varchar(255) NOT NULL,
prenom_acteurs varchar(255) NOT NULL,
date_naissance_acteurs DATE NOT NULL
)
```

### Pour créer la table effectuer :
```sql
CREATE TABLE effectuer (
id_effectuer int NOT NULL PRIMARY KEY AUTO_INCREMENT,
nom_role_effectuer varchar(255) NOT NULL,
prenom_role_effectuer varchar(255) NOT NULL,
role_acteur_effectuer varchar(255) NOT NULL,
id_films int NOT NULL,
id_acteurs int NOT NULL,
CONSTRAINT FK_films_effectuer
FOREIGN KEY (id_films)
REFERENCES films(id_films),
CONSTRAINT FK_acteurs_effectuer
FOREIGN KEY (id_acteurs)
REFERENCES acteurs(id_acteurs)
)
```

### Pour créer la table ajouter :
```sql
CREATE TABLE ajouter (
id_ajouter int NOT NULL PRIMARY KEY AUTO_INCREMENT,
id_utilisateurs int NOT NULL,
id_films int NOT NULL,
CONSTRAINT FK_utilisateurs_ajouter
FOREIGN KEY (id_utilisateurs)
REFERENCES utilisateurs(id_utilisateurs),
CONSTRAINT FK_films_ajouter
FOREIGN KEY (id_films)
REFERENCES films(id_films)
)
```

