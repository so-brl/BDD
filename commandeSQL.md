Initialisation Commande SQL
* https://openclassrooms.com/fr/courses/918836-concevez-votre-site-web-avec-php-et-mysql/913893-phpmyadmin
* https://dev.mysql.com/doc/refman/8.0/en/user-names.html
* https://www.youtube.com/watch?v=4c50g_RXPZo
* https://www.sqltutorial.org/
*https://www.w3schools.com/sql/sql_join_inner.asp

## Création d’un utilisateur MySQL et octroi de tous les privilèges

  ````SHOW GRANTS FOR 'joe'@'office.example.com';
-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Grants for sonia@localhost                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, RELOAD, SHUTDOWN, PROCESS, FILE, REFERENCES, INDEX, ALTER, SHOW DATABASES, SUPER, CREATE TEMPORARY TABLES, LOCK TABLES, EXECUTE, REPLICATION SLAVE, REPLICATION CLIENT, CREATE VIEW, SHOW VIEW, CREATE ROUTINE, ALTER ROUTINE, CREATE USER, EVENT, TRIGGER, CREATE TABLESPACE, CREATE ROLE, DROP ROLE ON *.* TO `sonia`@`localhost`                                                                                                           |
| GRANT APPLICATION_PASSWORD_ADMIN,AUDIT_ADMIN,BACKUP_ADMIN,BINLOG_ADMIN,BINLOG_ENCRYPTION_ADMIN,CLONE_ADMIN,CONNECTION_ADMIN,ENCRYPTION_KEY_ADMIN,GROUP_REPLICATION_ADMIN,INNODB_REDO_LOG_ARCHIVE,PERSIST_RO_VARIABLES_ADMIN,REPLICATION_APPLIER,REPLICATION_SLAVE_ADMIN,RESOURCE_GROUP_ADMIN,RESOURCE_GROUP_USER,ROLE_ADMIN,SERVICE_CONNECTION_ADMIN,SESSION_VARIABLES_ADMIN,SET_USER_ID,SYSTEM_USER,SYSTEM_VARIABLES_ADMIN,TABLE_ENCRYPTION_ADMIN,XA_RECOVER_ADMIN ON *.* TO `sonia`@`localhost` |
+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)  



````

###Création de l 'utilisateur.
* CREATE USER 'nomUtilisateur'@'localhost' IDENTIFIED BY 'motDePasse';
* CREATE USER 'sonia'@'localhost' IDENTIFIED BY 'blogCampus';
###Accorder les accés.
**Accoerder tous les privilèges**
* ```` GRANT ALL PRIVILEGES ON * . * TO 'non-root'@'localhost';````
*````GRANT ALL PRIVILEGES ON * . * TO 'sonia'@'localhost';<br/>````
Pour que les changements prennent effet, appliquez immédiatement les privilèges en tapant la commande suivante:
<br/>````FLUSH PRIVILEGES;```` permet de remettre à jour les privilèges;

## Octroi de privilèges spécifiques pour un utilisateur MySQL 
*https://dev.mysql.com/doc/refman/8.0/en/privileges-provided.html#privileges-provided-summary
* ````
  GRANT [permission type] ON [database name].[table name] TO ‘non-root’@'localhost’;
  ````
  <br/>
 * Remplacer la valeur « type de permission » par le type de permission que vous souhaitez accorder au nouvel utilisateur.
  <br/>
 * spécifier les noms de base de données et de table
  <br/>
  ````* = sur tous ```` 
## MANIPULATION 
**Sélection sur une table :**
* Lister tous les articles : <br/>
``SELECT * FROM articles;``
* Lister les articles publiés depuis le « 01/01/2020 » qui ont une importance supérieur à 2 : <br/>
``SELECT `Importance`,`Date`,`Titre` FROM `articles` WHERE (`Date` >'2020-01-01') AND (`Importance` > 2)``
* Lister les articles visibles aujourd’hui, par date de publication décroissante  : <br/>
``SELECT`Titre`,`Date`,`DateFin` FROM `articles` WHERE (`DateFin`>'2020-01-22') ORDER BY `DateFin` DESC``
<br/>
**Sélection sur plusieurs tables:**
* Lister les articles avec le nom de leur catégorie : <br/>
``SELECT `Article_Titre`,`Categorie_Nom Categorie` FROM `articles_categories` WHERE 1``
* Lister tous les articles de la catégorie « Loisirs » : <br/>
``SELECT `Categorie_Nom Categorie`
  FROM `articles_categories` 
  WHERE (`Categorie_Nom Categorie`='Loisirs')``<br/>
* Compter les commentaires publiés par le pseudo « Matéo »:<br/>
``SELECT count(*) as `Auteurs_Pseudo`,`Titre`  FROM `articles` WHERE  (`Auteurs_Pseudo`= 'Mateo')``
* Lister les articles rédigés par le pseudo « Valentine » ou « Matéo » (afficher l’auteur) :<br/>
``SELECT `Titre`,`Auteurs_Pseudo` FROM `articles` WHERE(`Auteurs_Pseudo`= 'Mateo')OR  (`Auteurs_Pseudo`= 'Valentine')``
* Lister les articles visibles aujourd’hui avec le nom de la catégorie et le pseudo de l’auteur, par date de publication décroissante  :<br/>
``SELECT`Auteurs_Pseudo`,`Titre`,`Date`,`categorie_Nom Categorie`
  FROM `articles` 
  INNER JOIN  `articles_categories` 
  ON articles.Titre=articles_categories.Article_Titre 
  WHERE (`DateFin`>='2020-01-22')
  ORDER BY `Date` DESC``
<br/>
**Insertion et mise à jour et suppression de données**

* Ajouter un article avec comme catégorie « Loisirs » et l’auteur qui a le pseudo «Matéo » :<br/>
``INSERT INTO `articles`(`Titre`, `Texte`, `Date`, `Importance`, `DateFin`, `Auteurs_Pseudo`) 
  VALUES ('Article Inserer en commande SQL',' ctrop marrant blablablbablablabalbalablblablab','2020-01-22',5,'2020-03-22','Matéo');
  INSERT INTO `articles_categories`(`Article_Titre`, `Categorie_Nom Categorie`) 
  VALUES ('Article Inserer en commande SQL','Loisirs')``
* Renommer le pseudo « Valentine » par « Val »  :<br/>
``UPDATE `auteurs` SET `Pseudo`='Val' WHERE `Pseudo`='Valentin'``
* Supprimer les commentaires qui n’ont que “Sans avis” :<br/>
``DELETE FROM `commentaires` WHERE(`Texte`='Sans Avis')``
* Supprimer l’auteur avec un pseudo « Matéo » :<br/>
``DELETE FROM `auteurs` WHERE (`Pseudo`='Matéo')``