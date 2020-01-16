# Back-end

## Linux / Mac 

**Comment changer le propriétaire d'un fichier via la ligne de commande ?**

> ```bash
> sudo chown -R username:group directory
> ```
- **-R** pour que les changements soient récursifs sur l'ensemble des fichiers/dossiers enfants

**Comment lister les process en cours via la ligne de commande ?**
> ```bash
> ps aux
> # OR
> top
> ```

- `top` pour lister les process en temps réel et `ps` pour prendre un snapshop à un temps donné
- **a** montre les process de l'ensemble des utilisateurs
- **u** affiche une colonne contenant le nom de l'utilisateur / propriétaire du process
- **x** montre les process qui ne sont pas reliés au terminal

**Comment arrêter un processus en cours en ligne de commande ?**

> ```bash
> kill SIGNAL PID
> # OR
> killall SIGNAL NAME
> ```

- `kill` pour "tuer" des process bien précis via son PID. Plus efficace que `killall` qui peut parfois ignorer certains process.
- `killall` pour "tuer" un ou plusieurs process en utilisant un nom plutôt qu'un PID
- Il existe plusieurs types de signaux, permettant de faire différents type de `kill` suivant le code signal utilisé. Le signal par défaut permet d'arrêter le process spécifié, mais il existe d'autre signaux permettant par exemple de relancer un process en cours d'exécution (à la manière d'un restart). La commande `kill -l` offre une liste basique de l'ensemble des signaux disponibles.

## HTTP / HTTPS

**Définir les différents codes de réponses HTTP (200, 300, 400, 500)**

**Citer quelques codes de réponses HTTP et les définir (404, 401, 502, etc**)

**Définir les différents types de requêtes / protocoles HTTP (GET, POST, etc)**

**Quelle est la différence entre les protocoles `PUT` et `PATCH` ?**

**Quels sont les ports dédiés à HTTP et HTTPS ?**

**Quelles est la différence entre HTTP et HTTPS ?**

## SQL / NoSQL / Database

**Qu'est qu'un ORM ?**

ORM = Object-Relational-(Mapping / Mapper) 

Outils permettant de faire des calls SQL dans d'autres langages. Les ORMs offrent également d'autres fonctionnalités permettant de faire des calls SQLs complexes plus facilement (connection pooling, migrations, seeds, streams, etc). C'est aussi un moyen de "facilement" passer d'une technologie SQL à une autre (MySQL, PostgreSQL, etc). 

Le plus connu en PHP est Doctrine, ActiveRecord en Ruby. La plus part des autres ORMs font partie intégrante de frameworks globaux (Laravel, CakePHP, Django, Ruby on Rails).

**Quelle est la différence entre une base de données SQL et NoSQL ?**

La plus grande différence est que une BDD SQL est relationnelle, elle utilise des tables de relations, là où NoSQL utilise un système de clé-valeur. Cela offre plusieurs avantages / inconvénients : 
- Les bases de données SQL vont être plus pratiques car elles permettent de faire des requêtes beaucoup plus complexe, et ont une structure hiérarchique.
- Les bases NoSQL vont offrir moins de possibilités et sont moins rapide quand il s'agit de faire des requêtes complexes. Cependant elles sont beaucoup plus facile à scaler, facilitant la montée en charge. Beaucoup d'applications utilisent ce type de base de données pour des applications en temps réel, ou encore la mise en cache.

**À quoi sert `DROP TABLE` ?**

`DROP TABLE` permet de supprimer une table SQL.

**Quelle est la différence entre `DROP TABLE` et `TRUNCATE TABLE` ?**

`DROP TABLE` supprimer définitivement la table alors que `TRUNCATE TABLE` supprime uniquement son contenu (elle la vide).

**Qu'est-ce qu'un `index` en SQL ?**

Un index est une structure entretenue automatiquement, qui permet de localiser facilement des enregistrements dans un fichier.

De la même manière qu'un sommaire ou qu'un annuaire, l'index facilite et accélère la recherche d'informations dans la base en classant les références à une donnée de manière particulière.

**Qu'est-ce qu'une `PRIMARY KEY` ?**

Une `PRIMARY KEY` ou `ID` est une valeur unique associée à chaque entrée dans une table et qui permet de faire référence à cette entrée pour la lire, la modifier, le supprimer, etc.

**Qu'est-ce qu'une `FOREIGN KEY` ?**

Une `FOREIGN KEY` est une référence à une `PRIMARY KEY` d'une autre table. Elle permet de mettre en relation des entrées entre différentes tables.

## PHP

**Quelle est la différence entre une Interface et une Classe Abstraite ?**

**Quelle est la différence entre `private` `protected` et `public` ?**

**Qu'est-ce que Xdebug et à quoi sert-il ?**

**Avec quels outils peut-on faire des tests en PHP ?**

**En quoi Xdebug est utile pour faire des tests avec PHPUnit ?**

**Qu'est-ce que `composer` ?**

**Que peut-on faire avec composer ?**