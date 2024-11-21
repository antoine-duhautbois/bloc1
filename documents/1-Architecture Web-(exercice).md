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
![Xampp](https://i.ibb.co/PGXkpgG/Capture-d-cran-2024-11-21-181923.png)
![dev.local](https://i.ibb.co/4VZdzGx/Capture-d-cran-2024-11-21-185307.png)

# 9-CURL
##### requête GET vers l’url http://dev.local
```html
<!doctype html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Web local</title>
</head>
<body>
    <h1>TDs web</h1>
</body>
</html>
```
##### requête GET vers l’url http://dev.local/notExisting
```html
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>404 Not Found</title>
</head><body>
<h1>Not Found</h1>
<p>The requested URL was not found on this server.</p>
<hr>
<address>Apache/2.4.58 (Win64) OpenSSL/3.1.3 PHP/8.2.12 Server at dev.local Port 80</address>
</body></html>
```
# 10-Headers

| **En-tête**             | **Description**                                                                                                  | **Exemple**                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| **Host**                | Indicatif de l'hôte et du port visé. Il est essentiel d'identifier le serveur, en particulier en cas d'hébergement mutualisé. | `Host: www.example.com`                                     |
| **User-Agent**          | Détermine le client qui réalise la demande (navigateur, bot, etc.)                       |User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64)`          |
| **Accept**              | Expose les différents types de contenu que le client est disposé à accueillir.   | `Accept: text/html, application/json`                       |
| **Accept-Language**     | Indique la langue préférée du client pour le contenu.                                                           | `Accept-Language: en-US, fr-FR;q=0.8`                       |
| **Accept-Encoding**     | Diffère les formats d'encodage que le client peut utiliser, tels que gzip ou deflate.| `Accept-Encoding: gzip, deflate`                            |
| **Authorization**       | Transporte les informations d'authentification (Basic, Bearer token, etc.).                                     | `Authorization: Basic dXNlcjpwYXNzd29yZA==`                 |
| **Content-Type**        | Définit le type de contenu de la requête lorsqu'elle transporte des données (POST,etc.).                  | `Content-Type: application/json`                            |
| **Content-Length**      | Indique la taille du corps de la requête en octets.                                                             | `Content-Length: 349`                                       |
| **Cookie**              | Envoie des cookies au serveur pour maintenir la session ou transmettre des données spécifiques.                 | `Cookie: sessionId=abc123`                                  |
| **Referer**             | Spécifie l'URL de la page d'où provient la requête.                                                             | `Referer: https://www.google.com`                           |
| **Connection**          | Contrôle si la connexion reste ouverte après la requête.                                           | `Connection: keep-alive`                                    |
| **Cache-Control**       | Donne des directives sur la gestion du cache.                                         | `Cache-Control: no-cache`                                   |
| **Origin**              | Identifie l'origine de la requête pour les requêtes cross-origin.                                               | `Origin: https://example.com`                               |
| **Upgrade-Insecure-Requests** | Demande si le contenu HTTP peut être mis à jour vers HTTPS.                                               | `Upgrade-Insecure-Requests: 1`                              |

