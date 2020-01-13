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
- Il existe plusieurs types de signal, permettant de faire différents type de `kill` suivant le code signal utilisé. Le signal par défaut permet d'arrêter le process spécifié, mais il existe d'autre signaux permettant par exemple de relancer un process en cours d'exécution (à la manière d'un restart). La commande `kill -l` offre une liste basique de l'ensemble des signaux disponibles.

## HTTP / HTTPS

**Définir les différents codes de réponses HTTP (200, 300, 400, 500)**

**Citer quelques codes de réponses HTTP et les définir (404, 401, 502, etc**)

**Définir les différents types de requêtes / protocoles HTTP (GET, POST, etc)**

**Quelle est la différence entre les protocoles `PUT` et `PATCH` ?**

**Quels sont les ports dédiés à HTTP et HTTPS ?**

**Quelles est la différence entre HTTP et HTTPS ?**

## SQL / NoSQL / Database

**Qu'est qu'un ORM ?**

**Quelle est la différence entre une base de données SQL et NoSQL ?**

**À quoi sert `DROP TABLE` ?**

**Quelle est la différence entre `DROP TABLE` et `TRUNCATE TABLE` ?**

## PHP

**Quelle est la différence entre une Interface et une Classe Abstraite ?**

**Quelle est la différence entre `private` `protected` et `public` ?**

**Qu'est-ce que Xdebug et à quoi sert-il ?**

**Avec quels outils peut-on faire des tests en PHP ?**

**En quoi Xdebug est utile pour faire des tests avec PHPUnit ?**

**Qu'est-ce que `composer` ?**

**Que peut-on faire avec composer ?**