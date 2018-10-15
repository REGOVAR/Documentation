# Installation avec SaltStack

Référez-vous au [README](https://github.com/REGOVAR/ServerConfiguration/blob/master/README.md) de la configuration utilisée pour le déploiement au CHU d'Angers et de Nancy.

Une fois le serveur installé, vous pouvez:

 * démarrer Regovar :
```sh
sudo systemctl start regovar
```

 * l'arrêter :
```sh
sudo systemctl stop regovar
```

 * faire en sorte qu'il se lance au démarrage du serveur :
```sh
sudo systemctl enable regovar
```

 * vérifier s'il est bien démarré et depuis combien de temps :
```sh
sudo systemctl status regovar
```

 * lire son journal :
```sh
sudo journalctl -u regovar
```
