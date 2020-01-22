Initialisation Commande SQL
* https://openclassrooms.com/fr/courses/918836-concevez-votre-site-web-avec-php-et-mysql/913893-phpmyadmin


## Création d’un utilisateur MySQL et octroi de tous les privilèges

###Création de l 'utilisateur.
* CREATE USER 'nomUtilisateur'@'localhost' IDENTIFIED BY 'motDePasse';
* CREATE USER 'sonia'@'localhost' IDENTIFIED BY 'blogCampus';
###Accorder les accés.
**Accoerder tous les privilèges**
* ```` GRANT ALL PRIVILEGES ON * . * TO 'non-root'@'localhost';````
*````GRANT ALL PRIVILEGES ON * . * TO 'sonia'@'localhost';<br/>````
Pour que les changements prennent effet, appliquez immédiatement les privilèges en tapant la commande suivante:
<br/>````FLUSH PRIVILEGES;````

## Octroi de privilèges spécifiques pour un utilisateur MySQL 
* ````
  GRANT [permission type] ON [database name].[table name] TO ‘non-root’@'localhost’;
  ````
  Remplacer la valeur « type de permission » par le type de permission que vous souhaitez accorder au nouvel utilisateur.