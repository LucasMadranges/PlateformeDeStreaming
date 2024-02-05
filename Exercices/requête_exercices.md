# Les différentes requêtes pour les exercices

## Exercice 1 - Les titres et dates de sortie des films du plus récent au plus ancien :
```sql
SELECT titre_films , date_sortie_films
FROM films f
ORDER BY date_sortie_films DESC;
```
## Exercice 2 - Les noms, prénoms et âges des acteurs/actrices de plus de 30 ans dans l'ordre alphabétique :
```sql
SELECT nom_acteurs, prenom_acteurs, TIMESTAMPDIFF(YEAR, date_naissance_acteurs , NOW()) AS age
FROM acteurs
GROUP BY nom_acteurs , prenom_acteurs, date_naissance_acteurs
HAVING age > 30
ORDER BY nom_acteurs , prenom_acteurs ;
```
## Exercice 3 - La liste des acteurs/actrices principaux pour un film donné :
```sql
SELECT titre_films , date_sortie_films
FROM films
ORDER BY date_sortie_films DESC;
```
## Exercice 4 - La liste des films pour un acteur/actrice donné :
```sql
SELECT nom_acteurs AS nom, prenom_acteurs AS prenom, titre_films
FROM effectuer
         INNER JOIN acteurs ON effectuer.id_acteurs = acteurs.id_acteurs
         INNER JOIN films ON effectuer.id_films = films.id_films
WHERE acteurs.id_acteurs = 1;
```
## Exercice 5 - Ajouter un film :
```sql
INSERT INTO films (titre_films , duree_films , date_sortie_films, id_realisateurs)
VALUES ('Interstellar', '02:49:00', '2014-11-15', 4);
```
## Exercice 6 - Ajouter un acteur :
```sql
INSERT INTO acteurs (nom_acteurs , prenom_acteurs , date_naissance_acteurs)
VALUES ('Smith', 'Will', '1968-09-25');
```
## Exercice 7 - Modifier un film :
```sql
UPDATE films SET titre_films  = "Un nouveau nom"
WHERE id_films  = 6;
```
## Exercice 8 - Supprimer un acteur :
```sql
DELETE FROM acteurs WHERE nom_acteurs = 'Smith'
```
## Exercice 9 - Afficher les 3 derniers acteurs/actrices ajouté(e)s :
```sql
SELECT * FROM acteurs
ORDER BY id_acteurs DESC
    LIMIT 3;
```
## Exercice 10 - Afficher le film le plus ancien :
```sql
SELECT * FROM films
ORDER BY date_sortie_films ASC
    LIMIT 1;
```
## Exercice 11 - Afficher l’acteur le plus jeune :
```sql
SELECT * FROM acteurs
ORDER BY date_naissance_acteurs DESC
    LIMIT 1;
```
## Exercice 12 - Compter le nombre de films réalisés en 1990 :
```sql
SELECT COUNT(date_sortie_films)
FROM films
WHERE YEAR(date_sortie_films) = 1990
```

## Exercice 13 - Faire la somme de tous les acteurs ayant joué dans un film :
```sql
FROM films 
LEFT JOIN effectuer ON films.id_films = effectuer.id_films
GROUP BY titre_films
```