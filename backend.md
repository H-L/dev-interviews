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

- **1xx** Informationnal
- **2xx** Success
- **3xx** Redirection
- **4xx** Client Error
- **5xx** Server Error

**Citer quelques codes de réponses HTTP et les définir (404, 401, 502, etc**)

- **200** OK = La requête a réussi
- **301** Moved Permanently = Redirection permanente de l'adresse spécifiée pour la requête
- **404** Not Found = La ressource demandée n'a pas été trouvé sur le serveur
- **500** Internal Server Error = Le serveur a rencontré une erreur qui l'empêche de répondre correctement et ne concerne pas d'autres erreurs 500 identifiables

**Définir les différentes méthodes HTTP (GET, POST, etc)**

- **POST** La requête envoi un objet nécessaire pour obtenir une réponse
- **GET** Requête demandant la lecture ou de retrouver une ressource
- **PUT** Requête de mise à jour complète d'une ressource
- **PATCH** Requête de mise à jour partielle d'une ressource
- **DELETE** Requête de suppression d'une ressource

**Quelle est la différence entre les méthodes `PUT` et `PATCH` ?**

Le protocole `PUT` met à jour l'ensemble de la ressource concernée, et doit donc contenir la structure et les donées exactes de cette même ressource.
Le protocole `PATCH` permet de mettre à jour seulement une partie d'une ressource, sans avoir à réécrire / re-spécifier l'ensemble de sa structure et de ses données.

**Quels sont les ports dédiés à HTTP et HTTPS ?**

- **HTTP** Port `80`
- **HTTPS** Port `443`

**Quelles sont les différences entre HTTP et HTTPS ?**

`HTTP` signifie `HyperText Transfert Protocol` et le `S` signifie `Secure`.

Le protocole `HTTPS` est une version plus avancée et sécurisée de `HTTP`. Il permet de sécuriser les échanges de données entre le serveur et le navigateur.

Le cryptage des communications en `HTTPS` est basé sur un protocole SSL/TLS.

`HTTPS` est souvent considéré comme plus rapide, mais ce n'est pas totalement vrai. Ce qui permet à `HTTPS` d'être plus performant est basé sur 2 points :
- Les serveurs supportant `HTTPS` supportent généralement `HTTP2.0` qui offre un gain de performance par rapport à `HTTP1.0`
- Si `HTTPS` est activé, la plus part des navigateurs pourront proposer des `Services Workers` qui accélèrent le chargement des sites pour les utilisateurs fréquents (support offline, chargement plus rapide des assets des sites et adresses visités, etc).

**Qu'est-ce qu'un Service Worker ?**

Un [Service Worker](https://developers.google.com/web/fundamentals/primers/service-workers/) est un script exécuté par le navigateur en tâche de fond, de manière séparée du reste de la page Web. Les Service Worker comprennent de nombreuses fonctionnalités telles que les Push Notifications ou la géolocalisation.

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