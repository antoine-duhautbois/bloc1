# 1-Méthodes GET et POST
##### La différence entre Get et POST est que GET passe les réponses saisies via l'URL tandis que la méthode POST passe les paramétres dans le corps de la requête.
# 2-Comparaison méthodes
| Comparatif : | Visibilité   |Marque-page et historique de navigation |Cache et fichier log du serveur| Longueur des données |
| ------- | -------- | ------|------|--------|
| Méthode GET  | L'utilisateur peut le voir dans le champ d'adresse.|Les paramètres de l'URL sont enregistrés ensemble avec l'URL.|Les paramètres de l’URL sont sauvegarder sans protection de chiffrement |  	Limitée , jusqu'à 2048 caractères | 
| Méthode POST| L'utilisateur ne le vois pas    |L’URL est enregistrée sans paramètres URL. |Les paramètres de l’URL ne sont pas sauvegarder automatiquement. | Pas de limite |
# 3-Extensible
##### Le protocole http est extensible car il peut avoir un en-tête personnalisés appelés (headers).
# 4-Sans état
##### Le concept de « protocole sans état » implique que le HTTP ne garde aucune information entre deux requêtes successives. Chaque demande d'un client adressée à un serveur est distincte des autres.
# 5-URL
##### Exemple : https://www.example.com:443/dossier/page.html?id=123&lang=fr

##### https:// | Son rôle est de spécifiée le protocole utilisé pour accéder à la ressource.
##### www.example.com | Son rôle c'est qu'il identifie le serveur sur lequel la ressource est hébergée.
##### :443 | Son rôle c'est que c'est le point d'entrée sur le serveur pour accéder à la ressource. Il n'est pas obligatoire de le mettre.
##### /dossier/page.html | Son rôle c'est d'indiqué l'emplacement spécifique de la ressource sur le serveur.
##### ?id=123&lang=fr | Son rôle c'est que c'est une chaîne de paramètres envoyés au serveur pour fournir des informations supplémentaires. lang=fr signifie que la page doit se charger en français.
# 6-Codes Status
##### 200 : signifie le succès de la requète | Exemple : 200 OK
##### 301 et 302 : redirection, respectivement permanente et temporaire | Exemple : 301 Moved Permanently
##### 4xx : signifie qu'il y'a une erreur Client | Exemple : 404 Not Found
##### 500, 502 et 503 :signifie qu'il y'a une erreur Serveur | Exemple : 500 Internal Server Error
# 8-Installation Apache & configuration
# 9-CURL
# 10-Headers
