# Les différentes requêtes pour insérer les données

## Données de la table réalisateurs :
```sql
INSERT INTO realisateurs  (nom_realisateurs, prenom_realisateurs, date_naissance_realisateurs)
VALUES ('Ruben', 'Fleischer', "1974-10-31"),
		('Tarantino', 'Quentin', "1963-03-27"),
       ('Kershner', 'Irvin', "1923-04-29"),
       ('Nolan', 'Christopher', "1970-07-30"),
 ('Spielberg', 'Steven', "1946-12-18"),
		('Cameron', 'James', "1954-08-16"),
       ('Kubrick', 'Stanley', "1928-07-26"),
       ('Jackson', 'Peter', "1961-10-31");
```

## Données de la table films :
```sql
INSERT INTO films (titre_films , date_sortie_films , id_realisateurs, duree_films)
VALUES ('Venom: Let There Be Carnage', '2021-10-20', 1, '01:37:00'),
       ('Once Upon a Time… in Hollywood', '2019-07-26', 2, '02:41:00')
    ('Star Wars: Episode V - The Empire Strikes Back', '1980-08-20', 3, '02:04:00'),
('Oppenheimer', '2023-07-19', 4, '03:01:00'),
('Jurassic Park', '1993-06-20', 5, '02:08:00'),
('Avatar: The Way of Water', '2022-12-14', 6, '03:02:00'),
('2001: A Space Odyssey', '1968-09-27', 7, '02:36:00'),
('The Hobbit: An Unexpected Journey', '2013-11-13', 8, '02:49:00')
```

## Données de la table acteurs :
```sql
INSERT INTO acteurs  ( nom_acteurs , prenom_acteurs  , date_naissance_acteurs )
VALUES ('Hardy', 'Tom', '1977-09-15'),
       ('DiCaprio', 'Leonardo', '1974-11-11'),
       ('Dicks', 'John', '1947-07-23'),
       ('Neill', 'Sam', '1947-09-14'),
       ('Worthington', 'Sam', '1976-08-02'),
       ('Serkis Ashbourne', 'Louis', '2004-12-24'),
       ('Murphy', 'Cillian', '1976-05-25'),
       ('Freeman', 'Martin', '1971-09-08')
```

## Données de la table utilisateurs :
```sql
INSERT INTO utilisateurs  (nom_utilisateurs, prenom_utilisateurs, date_naissance_utilisateurs, adresse_mail_utilisateurs, mot_de_passe_utilisateurs, role_utilisateurs)
VALUES ('Madranges', 'Lucas', '2003-02-04', 'lucas.madranges@my-digital-school.org', 'CECIESTUNMOTDEPASSESUR06803&!', 'admin'),
       ('TestNom', 'TestPrenom', '1999-12-23', 'test@test.test', 'CECIESTUNtestMOTDEPASSE', 'users')
```

## Données de la table effectuer :
```sql
INSERT INTO effectuer (nom_role_effectuer, prenom_role_effectuer, role_acteur_effectuer, id_films, id_acteurs)
VALUES ('', 'Bilbo', 'principal', 8, 8),
VALUES ('Oppenheimer', 'Robert', 'principal', 1, 1),
    ('Dalton', 'Rick', 'principal', 3, 3),
    ('Captain', 'Lennox', 'secondaire', 4, 4),
    ('', 'Venom', 'principal', 2, 2),
    ('Grant', 'alan', 'principal', 5, 5),
    ('Sully', 'Jack', 'principal', 6, 6),
    ('', '', 'secondaire', 7, 7)
```

## Données de la table ajouter :
```sql
INSERT INTO ajouter (id_utilisateurs, id_films)
VALUES (3, 1),
       (3, 5),
       (3, 6),
       (4, 2),
       (4, 8),
       (4, 7)
```

