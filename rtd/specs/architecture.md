
## Architecture N-tiers
Pour répondre au besoins, Regovar doit être conçu comme une application Client-Serveur. Mais à cause du pérmiètre fonctionnel étendu, et du niveau d'exigence demandé concernant le déployement, la maintenance et la prise en compte de la montée en charge, une architecture N-tiers a été imaginé.  

Pour rappel, une architecture N-tiers, à l'instar d'une architecture 3-tiers réparti les composants du système en 3 couches superposées :
 * une couche *serveur de données* qui fournit au système la capacité de stocker l'information;
 * une couche *serveur d'application* (appelé middleware) qui va exposer un certains nombre de service répondant à des besoins métiers;
 * une couche *client* qui, via une interface graphique, va permettre à un utilisateur d'accéder aux services exposés par le middleware.

La particularité de l'architecture N-tiers est que le serveur d'application est lui-même éclaté en de multiples services ou modules, plus petits, plus facile à concevoir, développer, maîtriser et maintenir.




## Composants logiciels
Cette section présente le système dans son ensemble, et comment les différents composants sont reliés entre eux.

![Architecture de l'application Regovar](https://raw.githubusercontent.com/REGOVAR/Documentation/master/rtd/assets/img/archi_system.png)

### Zones 
Trois zones distinctes sont identifiées dans le système Regovar:
 * **LAN ORGANIZATION** : il s'agit typiquement de l'intranet du CHU ou du laboratoire qui souhaite utiliser Regovar. Regovar est prévu pour être déployé sur un réseau privé et sécurisé comme l'intranet d'un hopital ou un réseau local.
 * **WORLD WILD WEB** : l'Internet mondiale, vaste et sauvage ! Un grand nombre d'outils et base de données publiques sont accessibles directement en ligne via Internet. Regovar en utilise un certains nombre.
 * **PUBLIC SHARING SERVER** : Le serveur publique de partage de donnée de Regovar. Il s'agit d'un serveur en théorie accessible par toutes les organisations utilisant Regovar souhaitant faciliter leur collaboration en partager certaines données (statistiques sur les variants/phénotypes, pipelines, etc).
 
A l'intérieur de ces zones, les composants on été regroupés en 3 groupes définissant des entités logiciels bien distinctes :
 * **Regovar Server** : regroupe le coeur du système Regovar;
 * **Sharing Server** : regroupe tout ce qui concerne le système de partage de données entre différents *Regovar Server*;
 * **Monitoring Broker** : les *monitoring broker* ont pour rôle d'aggréger des flux de logs dans une même base de données afin de faciliter par la suite leur exploitation.


### Sous-Systèmes (SS_)
En vert sont représentés les sous-systèmes de Regovar. A la manière des micros services, ce sont des briques logicielles plus petites et autonomes dans une certaine mesure, qui vont assurer un périmètre fonctionnel réduit et bien défini.
 * **SS_REGOVAR_SERVER** : Le coeur de Regovar, c'est actuellement lui qui gère toutes les fonctionalitées métiers de l'application. A l'avenir, ce sous-système gagnera à être lui aussi divisé en modules plus petits afin de faciliter sa maintenance et ses évolutions futures;
 * **SS_REGOVAR_GUI** : l'application graphique permettant à n'importe quel utilisateur d'accéder à Regovar. Il s'agit d'un client léger, facilement accessible via un navigateur web;
 * **SS_REGOVAR_CLI** : Regovar est aussi utilisable via des lignes de commandes afin de permettre aux administrateurs et aux scripts automatiques d'interragir plus facilement;
 * **SS_REGOVAR_DATABASE** : la base de donnée locale de Regovar. Se référer à la section 5 des spécifications : [Modèle de données](database.md) pour plus de détails;
 * **SS_MONITORING_BROKER** : comme vu précédemment, le monitoring broker permet de collecter, stocker des logs;
 * **SS_SHARING_SERVER** : permet à la fois de récolter et partager certaines données des *Regovar Server*;
 * **SS_SHARING_GUI** : une interface graphique pour que les utilisateurs puissent facilement consulter les données collectées par le *Sharing Server*;
 * **SS_SHARING_CLI** : une interface en ligne de commande pour les administrateurs systèmes;
 * **SS_SHARING_DATABASE** : la base de donnée du *Sharing Server*.


### Systèmes coopérants (CS_)
En gris sont représentés les systèmes dit "coopérants". Il s'agit de composants extérieurs, souvent génériques, avec lesquels les sous-systèmes de Regovar vont interragir.
 * **CS_TIERS_GENETICS_SERVICES** : bases de données et outils en lignes que Regovar utilise (OMIM, ORPHANET, Pubmed, ...);
 * **CS_USER_PIPELINES** : Regovar permet à ses utilisateurs d'encapsuler leurs pipelines dans des containers pour ensuite permettre à tous de les utiliser plus facilement, voir automatiquement. Pour cela les containeurs devront implémenter l'interface *IF_PIPELINE_ORCHESTRATION*;
 * **CS_ARCHIVE_SERVICE** : l'archivage des données de Regovar est laissé aux administrateurs qui pourront s'appuyer sur l'interface *IF_ORCHESTRATION* si besoin pour automatiser certaines tâches avec des scripts;
 * **CS_SEQUENCER** : les séquenceurs qui vont fournirs les données de bases. Là encore, on laisse le soin aux utilisateurs d'importer eux-mêmes ces données dans Regovar via l'interface graphique. A noter que comme pour l'archivage, il est aussi possible d'automatiser cette tâche avec des scripts via l'interface *IF_ORCHESTRATION*; 
 * **CS_MAIL_SERVICE** : si Regovar est connecté à un serveur de mail, il sera en capacité de notifier les utilisateurs lorsque certains événements se produiront;
 * **CS_USER_DIRECTORY** : par defaut Regovar sait gérer ses propres utilisateurs, mais il est possible de le relier à un annuaire externe (par exemple LDAP) pour qu'il l'utilise pour identifier et authentifier les utilisateurs;
 * **CS_LOGS_SERVICE** : si l'organisation le désire, les logs de Regovar peuvent être redirigés vers un système tierce de supervision;
 * **CS_MONITORING_SERVICE** : Regovar peut être configuré pour collecter certaines données des outils monitorant le système, permettant ainsi à ses utilisateurs de connaître l'état (de surcharge) sur serveur et des pipelines.

### Interfaces (IF_)
En bleu sont représentées les interfaces. Elles sont là afin de définir un protocole d'échange entre plusieurs Sous-systèmes et/ou Systèmes coopérants. A noter que lorsque le liens entre une interface et un sous-système est vert, celà signifie que c'est ce sous-système qui implémente et expose cette interface.
 * **IF_ORCHESTRATION** : 
 * **IF_PIPELINE_ORCHESTRATION** : 
 * **IF_LOGS** : 
 * **IF_LOGS_EXPORT** : 
 * **IF_USER_DIRECTORY** : 
 * **IF_SHARING** : 
 * **IF_MAIL** : 
 * **IF_MONITORING** : 
 
### Relations entre les composants

Intéressont nous maintenant aux comminications entre les différents composants listées précédemment et les protocoles utilisés quand c'est le cas. Les numéros ci-dessous réfèrent aux numéros cerclés en jaune sur le schéma.
 1. **HTTP(S)/WS(S)** : l'interface *IF_ORCHESTRATION* est une API REST. Le protocole utilisé par le client *SS-REGOVAR_GUI* pour communiquer avec est donc HTTP et les Websockets (WS) principalement utilisé pour les push notifications à l'initiatives du serveur;
 2. **HTTP(S)** : comme pour *SS-REGOVAR_GUI*, *SS-REGOVAR_CLI* utilise HTTP. Cependant 
 3. **PostgreSQL** : connection locale à la base de donnée *PostgreSQL*;
 4. **IMAP** : protocole générique employé pour envoyer des mails;
 5. **LDAP** : 
 6. **Syslog** : 
 7. **HTTP(S)** : 
 8. **HTTP(S)** : 
 9. **HTTP(S)** : la majorité des outils en ligne expose une API REST;
 10. **Syslog / Custom** : 
 11. **Custom** : 
 12. **REGOVAR_USER** : 
 13. **Custom** : 
 14. **REGOVAR_ADMINISTRATOR** : 
 15. **Custom** : 
 16. **HTTP(S)** : 
 18. **HTTP(S)** : 
 19. **WWW_USER** : 
 20. **SHARING_SERVER_ADMINISTRATOR** : 
 
 
