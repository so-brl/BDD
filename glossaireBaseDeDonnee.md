 # GLOSSAIRE <br/>
 ## BASE DE DONNEES <br/>
 ### Ressources <br/>
 * https://fr.wikibooks.org/wiki/Les_bases_de_donn%C3%A9es/Le_vocabulaire_de_base_des_BDD
 * https://fr.wiktionary.org/wiki/Cat%C3%A9gorie:Lexique_en_fran%C3%A7ais_des_bases_de_donn%C3%A9es
 
* **Base de données** : <br/>
Système d'organisation de l'information conçu pour une localisation et une mise à jour rapide et facile des données.
<br/>
Les données à numériséer sont appelées des "enregistrements".

* **Enregistrements** : <br/>
Regroupes l'ensembles des informations liées à une personnes, object ...<br/>
Définir un enregistrement , c'est définnir l'ensembles des attributs qu'il contient.

* **Les modèles de données**  : <br/>
 Dans les cas les plus simples, on peut mémoriser chaque liste dans un fichier.le senregistrements y  sont placées les uns à la suite des autres.
 Le stockage d'enregistrement ce font les un à la suite des autres. On ne peut placer de nouveaux enregistrment entre 2 exitant. <br/>
 Les enregristrement n'ont pas de liens les un avec les autres. C'est au programme de  de creer les liens entre les données et entres les fichiers. Cela ce fait nativement grace aubase de données. Grace au SGBD, le rangement des des informations dans un fichier n 'est pas a spécifier par le prgrammeur. 
 Le SGBD gère la manière de ranger les informations sur le disque dur. Mais leur intérêt principal est de modéliser les relations entre chaque liste d'enregistrement efficacement, d'une manière qui permet de traiter les données rapidement. 
  
 * **Modèles relationnel**  : <br/>
Type de base de données où les données sont liées à d'autres informations au sein des bases de données.Les bases de données relationnelles sont composées d’un ensemble de tables qui peuvent être accessibles et reconstruites de différentes manières, sans qu'il soit nécessaire de  réarranger ces tables de quelque façon que ce soit. Les instructions SQL vont être utilisées pour interroger de façon interactive les données contenues dans la base de données relationnelle.

Type de relation : Nbre de relation entre 2 table, cardinalité;
 
* **Les tables** : <br/>
Liste de données.<br/>
Lieux où sont stockés les enregistrements et leurs attibuts.
Les attributs de même nom et type sont placés sur une même colonne, les enregistrement se font ligne par ligne.<br/>
Il existe un vocabulaire assez précis pour nommer les enregistrements, colonnes et autres particularités d'une table. Ceux-ci sont illustrés dans les deux schémas ci-dessous. 
![alt text](https://upload.wikimedia.org/wikipedia/commons/a/ae/Figure_structure_relationnelle.png "nommer les enregistrements")
![alt text](https://upload.wikimedia.org/wikipedia/commons/f/fd/Table_relationnel.png "nommer les enregistrements")

* **Attributs** : <br/>
Chaque enregistrement est un regroupement d'attribut, chaque attiribut étant une information.<br/>
Un attribut ne peut pas être décomposé en informations plus simples. <br/>
Les attributs sont équivalents aux variables, du language de programmation. 

* **Les différents types de données/attributs** : <br/>
les valeurs que peuvent prendre chaque attribut, sont définies par des types.<br/>
Les types autorisés par les systèmes de gestion de données sont ceux couramment utilisés en informatique<br/>
Exemple: <br/>
-- son nom : chaine de caractère ;<br/>
-- son prénom : chaine de caractère ;<br/>
-- son adresse : chaine de caractère ;<br/>
-- le numéro de la commande : nombre entier ;<br/>
-- sa taille : nombre à virgule ;<br/>
-- on poids : nombre à virgule ;<br/>
-- son âge : nombre entier ;<br/>
-- son groupe sanguin : chaine caractère ;<br/>
-- son groupe rhésus : booléen ;<br/>
-- sa tension artérielle : nombre à virgule ;<br/>
-- image : fichier binaire; <br>

Choisir un mauvais type de donnée pourrait entraîner :
-- Un gaspillage de mémoire (ex. : si vous stockez de toutes petites données dans une colonne faite pour stocker de grosses quantités de données) ;<br/>
-- Des problèmes de performance (ex. : il est plus rapide de faire une recherche sur un nombre que sur une chaîne de caractères) ;<br/>
-- Un comportement contraire à celui attendu (ex. : trier sur un nombre stocké comme tel, ou sur un nombre stocké comme une chaîne de caractères ne donnera pas le même résultat) ;<br/>
-- L'impossibilité d'utiliser des fonctionnalités propres à un type de données (ex. : stocker une date comme une chaîne de caractères vous prive des nombreuses fonctions temporelles disponibles).
<br/>

* **Tuple**:<br/>
Tuple = ligne = enregistrement

* **n-uplet**:<br/>
n le nombre d'attributs dans cette ligne

* **Valeur NULL**:<br/>
Dans certains cas, il arrive que certaines informations ne soient pas connues lorsqu'on créer l'enregistrement. 
On doit alors remplir l'attribut correspondant par une valeur qui indique que l'attribut a une valeur inconnue,
que l'attribut n'a pas été rempli. Cette valeur est appelée la **valeur NULL**.<br/>
Par exemple :
-- nom de famille : Braguier ;<br/>
-- premier prénom : Jean-Paul ;<br/>
-- second prénom : NULL ;<br/>
-- troisième prénom : NULL ;<br/>
-- etc.<br/>

* ** Rendre une donnée obligatoire**:<br>
Nom_colonne : NOT NULL ; <br >
NOT NULL DEFAULT: si pas de valeur insérée, une valeur par défaut est appliquée.

* **Clé primaire :** <br/>
Identifiant unique dans une table constituée par un ou plusieurs champs de cette table. Cette identifiant cible des attibutes unique dans la table 
(Exemple : Colonne des numéro de client / Colonnes des numéro de commandes / Commande des articles)

* **Clé étrangère**  : <br/>
Champ spécifique d'une table correspondant à un identifiant unique sur une autre table (clé primaire) permet de garantir la cohérence des données.. 

* **Index** : <br/>
Structure de données utilisée et entretenue par le SGBD pour lui permettre de retrouver rapidement les données. L’index placé surune table va permettre au SGBD d'accéder très rapidement aux enregistrements, selon la valeur d'un ou plusieurs champs.

* **CRUD**: <br/>
Gérer des données dans une table demande de pouvoir faire quatre opérations de base : <br/>
--CREATE (créer) : créer une nouvelle ligne ; <br/>
--READ (lecture) : récupérer une ligne dans la table ;<br/>
--UPDATE (modifier) : modifier le contenu d'une ligne ou d'un attribut ;<br/>
--DELETE (supprimer) : supprimer une ligne devenue inutile.<br/>

Ces quatre opérations sont regroupées sous l'acronyme CRUD. 
