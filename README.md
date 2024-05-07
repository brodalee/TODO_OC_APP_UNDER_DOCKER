# Installation

```bash
docker compose up -d --build
```

Si la connexion se fait mal avec la BDD, il se pourrait que ça soit dû à un problème de type d'authentification.

Dans ce cas, dans le container de la BDD, il faudra modifier un fichier : 
Dans /etc/my.cbnf, ajouter la ligne suivante dans la section `[mysql]` : 
`default_authentication_plugin=mysql_native_password`

Redémarrer le container et ça devrait fonctionner.

L'application est disponnible [ici http://localhost:8080](http://localhost:8080)