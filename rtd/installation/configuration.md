# Configuration de Regovar


## Serveur

###Paramètres du config.py
Ci-dessous la liste des paramètres du fichier de configuration python du server. Pour la grande majorité vous pouvez laisser la valeur par défaut si vous suivez les mêmes réglages que ceux de la documentation. En revanche, il vous faudra impérativement mettre/générer vos propres réglages pour les entrées suivantes:
 - `HOST_P`
 - `PRIVATE_KEY32`
 - `OMIM_API_KEY`

| Clé | Type | Défaut | Description |
| --- | ---- | ------ | ----------- |
| `DEBUG` | `bool` | `False` | Affiche plus de logs et les affiches en plus directement dans la sortie "écran" de l'application |
| | | | |
| `HOST` | `string` | `127.0.0.1` | L'adresse utilisé par le serveur Regovar |
| `PORT` | `int` | `8500` | Le port utilisé par le serveur Regovar |
| `HOSTNAME` | `string` | `<HOST>:<PORT>` | Il s'agit des deux informations précédentes concaténée. C'est l'adresse qu'utilisera en interne aioHTTP pour le service Regovar. |
| `HOST_P` | `string` | `dev.regovar.org` | Il s'agit de l'adresse publique/externe par laquelle on accédera au serveur Regovar. En général, aioHTTP utilisé une adresse privée local (127.0.0.1) et c'est le serveur Apache ou NginX qui va faire office de proxy entre l'adresse publique utilisé par les utilisateur et l'adresse interne de Regovar.|
| | | | |
| `PRIVATE_KEY32` | `bool` | `False` | Il s'agit de la clés codée sur 32 caractères qui sera utilisé par le serveur pour crypter les mots de passe et les sessions des utilisateurs. Vous pouvez en générer une alétoirement sous linux avec la commande suivante : `$ date | md5sum` |
| `SESSION_MAX_DURATION` | `bool` | `86400` | La durée maximum avant que le serveur force une session utilisateur à expirer (et donc le forcer à se reconnecter). 86400 = 60*60*24 = 24 heures  |
| `OMIM_API_KEY` | `bool` | `False` | Votre clès pour accéder à l'api en ligne d'OMIM. Vous pouvez en obtenir une gratuitement à l'adresse suivante: https://omim.org/api. |
| | | | |
| `DATABASE_HOST` | `string` | `"localhost"` | L'adresse du serveur de la base de donnée postgresql |
| `DATABASE_PORT` | `int` | `5432` | Le port utilisé par le serveur postgresql |
| `DATABASE_USER` | `string` | `"regovar"` | L'utilisateur postgresql à utiliser  |
| `DATABASE_PWD` | `string` | `"regovar"` | Le mot de passe correspondant à cet utilisateur |
| `DATABASE_NAME` | `string` | `"regovar"` | Le nom de la base de donnée à utiliser |
| `DATABASE_POOL_SIZE` | `int` | `7` | Le nombre maximal de thread qui seront dédié à l'exécution des requêtes postgresql |
| `VCF_IMPORT_MAX_THREAD` | `int` | `7` | Le nombre maximal de thread qui seront alloué par le serveur lors du parsage et de l'import des données issuent d'un fichier VCF |
| | | | |
| `FILES_DIR` | `string` | `"/var/regovar/files"` | Le répertoire sur le serveur où seront stockés les fichiers |
| `TEMP_DIR` | `string` | `"/var/regovar/downloads"` | Le répertoire sur le serveur où seront stockés les fichiers temporaires ou en cours de téléchargement |
| `CACHE_DIR` | `string` | `"/var/regovar/cache"` | Le répertoire sur le serveur où seront stockés en cache certains résultats (comme les appels aux API public tiers: OMIM, Pubmed, ...). La durée de ce cache peut être modifiée avec le paramètre `CACHE_EXPIRATION_SECONDS` |
| `DATABASES_DIR` | `string` | `"/var/regovar/databases"` | Attention. Il ne s'agit de l'endroit pù sont stockés les bases de données postgresql. Il s'agit du répertoire où sont stockés les référentiels et les bases de données d'annotations (Hg19, Hg38, HPO,...). Ces bases de données seront accessibles par les pipelines exécutés dans les containers Docker/LXD afin de leur permettre un accès efficace à ces ressources.  |
| `PIPELINES_DIR` | `string` | `"/var/regovar/pipelines"` | Le répertoire où seront stockés les machines virtuelles (container docker ou LXD) créées pour les pipelines |
| `JOBS_DIR` | `string` | `"/var/regovar/jobs"` | Le répertoire où seront stockés les fichiers nécessaire à l'exécution d'une pipeline (fichier de config) ainsi que les résultats générés (outputs) |
| | | | |
| `CACHE_EXPIRATION_SECONDS` | `int` | `2592000` | La durée maximale de mise en cache d'un résultat. 30 jours (60*60*24*30) |
| `RANGE_DEFAULT` | `int` | `100` | Le nombre de résultat max retournés par défaut en cas de pagination. L'utilisateur peut forcer le serveur à en retourner plus par requête en spécifiant le paramètre `range` des requêtes |
| `RANGE_MAX` | `int` | `1000` | Le nombre maximum que l'utilisateur peut espérer récupérer en modifiant le paramètre `range` |
| | | | |
| `REGOVAR_DIR` | `string` | `.` | Le répertoire sur le serveur où est l'application Regovar  |
| `LOG_DIR` | `string` | `<REGOVAR_DIR>` | Le répertoire où seront stockés les logs  |
| `TEMPLATE_DIR` | `string` | `...` | Le répertoire où sont stockés les templates HTML  |
| `ERROR_ROOT_URL` | `string` | `<HOST_P>/errorcode/` | L'adresse qui sera utilisé par le serveur pour guider l'utilisateur à trouver l'aide automatique correspondant aux codes d'erreurs |
| `NOTIFY_URL` | `string` | `...` | L'adresse utilisé en interne par les containers Docker/LXD pour notifier le serveur de leur progression |
| | | | |
| `PIPELINE_DEFAULT_ICON_PATH` | `string` | `...` | L'icone par défaut utilisé pour les Pipelines quand ce dernier n'est pas fournis à l'installation.  |
| `MAX_JOB_RUNNING` | `string` | `5` | Le nombre maximum de pipeline qui pourront être exécuté en parallèle |
| `CONTAINERS_CONFIG` | `json` |  | Configuration du manager LXD. Voir la section dédiée.   |



###Paramètres en base de donnée

| Clé | Défaut | Description |
| --- | ------ | ----------- |
| `database_version` | `M.m.b` | Il s'agit de la version actuelle de la base de donnée. Vous ne devez en aucun cas modifier cette valeur. Elle est mis à jours par les développeurs quand le schéma de la base est modifié lors d'une évolution du logiciel. Elle permet de s'assurer que l'application est compatible avec la base de donnée utilisée. |
| `backup_date` | `AAAA-MM-DD HH:mm:ss` | La date à laquelle a été faite pour la dernière fois le backup des données de Regovar. Voir la section maintenance et l'usage d'un script d'archivage pour plus de renseignement. Cette information est ensuite visible à titre informatif dans le client QRegovar. |
| `stats_refresh_date` | `AAAA-MM-DD HH:mm:ss` |  La date à laquelle ont été mis à jour pour la dernière fois les statistiques internes de la base de donnée Regovar. Voir la section maintenance et l'usage d'un script de mise à jours des stats pour plus de renseignement. Cette information est ensuite visible à titre informatif dans le client QRegovar.  |



###Installer un nouveau référenciel




###Mettre à jour les données phénotype (HPO)

Très simple, il suffit de lancer la commande `make update_hpo`, et le script s'occupera pour vous de récupérer la dernière version de la base de donnée HPO et d'enregistrer ces données dans la base de donnée de Regovar. Les données HPO sont mises à jours environs tous les mois.



## Client (admin)

###Création de nouveau utilisateur



