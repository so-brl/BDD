 #GLOSSAIRE
 ##BASE DE DONNEES 
 ###Ressources 
 * https://fr.wikibooks.org/wiki/Les_bases_de_donn%C3%A9es/Le_vocabulaire_de_base_des_BDD
 
* **Base de données** : <br/>
Système d'organisation de l'information conçu pour une localisation et une mise à jour rapide et facile des données.
<br/>
Les donnéesà numériséer sont appellé des "enregistrements".

* **Les tables** : <br/>
Liste de données.<br/>
Lieux où sont stockés les enregistrements et leurs attibuts.
Les attributs de même nom et type sont placés sur une même colonne, less enregistrement se font ligne par ligne.

* **Enregistrements** : <br/>
Regroupes l'ensembles des informations liées à une personnes, object ...<br/>
Définir un enregistrement , c'est définnir l'ensembles des attributs qu'il contient.


* **Attributs** : <br/>
Chaque enregistrement est un regroupement d'attribut, chaque attiribut étant une information.<br/>
un attribut ne peut pas être décomposer en informations plus simples. <br/>
Les attributs sont équivalant au variables, du language de programmation. 


* **Type d'attribut** : <br/>
les valeurs que peuvent prendre chaque attribut, sont définnit par des types.<br/>
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
 
* **Valeur NULL**:<br/>
Dans certains cas, il arrive que certaines informations ne soient pas connues lorsqu'on crée l'enregistrement. 
On doit alors remplir l'attribut correspondant par une valeur qui indique que l'attribut a une valeur inconnue,
que l'attribut n'a pas été rempli. Cette valeur est appelée la **valeur NULL**.<br/>
Par exemple :
-- nom de famille : Braguier ;<br/>
-- premier prénom : Jean-Paul ;<br/>
-- second prénom : NULL ;<br/>
-- troisième prénom : NULL ;<br/>
-- etc.<br/>

 
 * **Les modèles de données**  : <br/>
 Dans les cas les plus simples, on peut mémoriser chaque liste dans un fichier.le senregistrements y  sont placées les uns à la suite des autres.
 Le stockage d'enregistrement ce font les un à la suite des autres. On ne peut placer de nouveaux enregistrment entre 2 exitant. <br/>
 Les enregristrement n'ont pas de liens les un avec les autres. C'est au programme de  de creer les liens entre les données et entres les fichiers. Cela ce fait nativement grace aubase de données. Grace au SGBD, le rangement des des informations dans un fichier n 'est pas a spécifier par le prgrammeur. 
 Le SGBD gère la manière de ranger les informations sur le disque dur. Mais leur intérêt principal est de modéliser les relations entre chaque liste d'enregistrement efficacement, d'une manière qui permet de traiter les données rapidement. 
 
  
 * **Modèles relationnel**  : <br/>
Les bases de données utilisent des méthodes assez distinctes pour représenter les relations entre informations, méthodes qui permettent de distinguer les BDD arborescentes, en réseau, relationnelles, déductives et orientées-objet. Les plus simples sont de loin les BDD en réseau et arborescentes.
 Celles-ci codent les relations entre listes par des pointeurs, chaque enregistrement pouvant faire référence à un autre, situé dans une autre liste. La différence entre BDD en réseau et arborescentes tient dans le fait que certaines relations sont interdites dans les BDD arborescentes, qui ont une forme d'arbre (non-binaire, le plus souvent). Le modèle relationnel sera vu plus loin : c'est lui que nous étudierons dans ce cours. Le fait est que toutes les BDDs actuelles utilisent le modèle relationnel. Les modèles orientés-objet et déductifs sont plus difficiles à décrire, du moins pour qui ne sait pas ce que sont les langages de programmation orientés-objet ou logiques. 
* BDD à pointeurs
![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Hierarchical_Model.svg/548px-Hierarchical_Model.svg.png "BDD à pointeurs")
![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/Network_Model.svg/542px-Network_Model.svg.png "BDD à pointeurs")
* BDD sans pointeurs
![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7c/Object-Oriented_Model.svg/598px-Object-Oriented_Model.svg.png "BDD sans pointeurs")
![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/d/da/Relational_Model.svg/543px-Relational_Model.svg.png "BDD sans pointeurs")

* **Le modèle relationnel**:<br/>

* **Clé étrangère**  : <br/>
Champ spécifique d'une table correspondant à un identifiant unique sur une autre table (clé primaire) permet de garantir la cohérence des données.. 


* **Clé primaire :** <br/>
Identifiant unique dans une table constituée par un ou plusieurs champs de cette table. Cette identifiant cible des attibutes unique dans la table 
(Exemple : Colonne des numéro de client / Colonnes des numéro de commandes / Commande des articles)


* **Index** : <br/>
Accélérateur de traitements (tri, recherche, ...), un index est une table A liée à une autre table B comprenant le minimum d'information permettant d'accéder rapidement aux informations de la table B, une table d'index comprend une clé de la table B et la position physique de cette clé dans la table B 

* **Relation** : <br/>
Concept de correspondance, une relation dans un ensemble est une proposition qui lie un certain nombre d'éléments, une relation dans une base de données est une table liée 


* **Les différents types de données** : <br/>

