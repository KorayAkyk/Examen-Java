# Examen-Java

Exercice d'examen de Java : gestion d'un hôtel avec Hibernate et une base MySQL.

## Ce que ça fait

- quatre entités : `Hotel`, `Chambre` (numéro, superficie, type, étage, hôtel), `Directeur` et `Salarie` (nom, prénom, salaire, directeur) ;
- une classe de service par entité (`HotelService`, `ChambreService`, `DirecteurService`, `SalarieService`) avec création, suppression, mise à jour, recherche par identifiant et liste complète ;
- `main.java` crée un directeur et des salariés, puis affiche le plus gros salaire.

## Technologies

Java 16, Maven, Hibernate 5.4 (`hibernate-core`), MySQL.

## Ce qu'il faut

JDK 16 ou plus récent, Maven et un serveur MySQL local.

## Lancer

```
mvn compile
```

Ce dépôt est une des versions de l'exercice (voir aussi Examen-Java2021 et JavaExam). Il ne contient pas de fichier `hibernate.cfg.xml`, que `HibernateUtil` attend pour se connecter. La classe `connexion.java` ouvre à la place une connexion JDBC directe vers MySQL. `main.java` n'est pas terminé : il utilise une variable `directeur1` non déclarée et importe `DirecteurService` et `SalarieService` depuis le mauvais paquet.

## Organisation

Le code est dans `src/main/java/korayakyurek/` : `Model/` (entités), `Service/` (accès aux données), `HibernateUtil.java`, `connexion.java` et `main.java`.
