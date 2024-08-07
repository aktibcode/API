# Chapitre : API PRATIQUE - HEADERS


# En-têtes :

**Les champs d'en-tête HTTP** sont des composants de la section d'en-tête des messages de requête et de réponse du protocole HTTP. Ils définissent les paramètres de fonctionnement d'une transaction HTTP.

```
//example of headers using postman

{
 'content-type': 'application/x-www-form-urlencoded',
 'user-agent': 'PostmanRuntime/7.22.0',
 accept: '*/*',
 'cache-control': 'no-cache',
 'postman-token': '35f27261-d4da-47d7-b540-9216d4fa694e',
 host: '127.0.0.1:3001',
 'accept-encoding': 'gzip, deflate, br',
 'content-length': '37',
 connection: 'keep-alive'
}
```

# En-têtes :

Les en-têtes et paramètres REST contiennent une multitude d'informations qui peuvent vous aider à détecter les problèmes lorsque vous les rencontrez. Les en-têtes HTTP sont une partie importante de la requête et de la réponse de l'API car ils représentent les métadonnées associées à la requête et à la réponse de l'API. Les en-têtes contiennent des informations pour :

1. Corps de la requête et de la réponse
2. Demande d'autorisation
3. Mise en cache des réponses
4. Cookies de réponse

Outre les catégories ci-dessus, les en-têtes HTTP contiennent également de nombreuses autres informations sur les types de connexion HTTP, les proxys, etc. La plupart de ces en-têtes sont destinés à la gestion des connexions entre le client, le serveur et les proxys et ne nécessitent pas de validation explicite par le biais de tests.

# En-têtes :

Les en-têtes sont principalement classés comme en-têtes de requête et en-têtes de réponse. Connaissez les principaux en-têtes de requête et de réponse. Vous devrez définir les en-têtes de requête lorsque vous envoyez la requête pour tester une API et vous devrez définir l'assertion par rapport aux en-têtes de réponse pour vous assurer que les bons en-têtes sont renvoyés.

Les en-têtes que vous rencontrerez le plus souvent lors des tests d'API sont les suivants. Vous devrez peut-être définir des valeurs pour ceux-ci ou définir des assertions par rapport à ces en-têtes pour vous assurer qu'ils transmettent les bonnes informations et que tout fonctionne correctement dans l'API :

**Autorisation :** contient des informations d’identification contenant les informations d’authentification du client pour la ressource demandée.

**WWW-Authenticate :** ce message est envoyé par le serveur s'il a besoin d'une forme d'authentification avant de pouvoir répondre avec la ressource demandée. Il est souvent envoyé avec un code de réponse 401, qui signifie « non autorisé ».

**Accept-Charset :** il s'agit d'un en-tête défini avec la demande et indiquant au serveur quels jeux de caractères sont acceptables par le client.

**Content-Type :** indique le type de média (texte/html ou texte/JSON) de la réponse envoyée au client par le serveur, cela aidera le client à traiter correctement le corps de la réponse.

**Cache-Control :** Il s'agit de la politique de cache définie par le serveur pour cette réponse, une réponse mise en cache peut être stockée par le client et réutilisée jusqu'au moment défini par l'en-tête Cache-Control.

# En-têtes :

![](https://i.imgur.com/MpbzOoZ.png)

L'en-tête HTTP contient des informations sur le corps HTTP et la requête/réponse.
Les informations sur le corps sont liées au contenu du corps, comme la longueur du contenu à l'intérieur du corps.
Les informations sur la requête/réponse sont des informations générales sur la requête/réponse et ne sont pas spécifiques au contenu du corps, par exemple à quelle heure la requête a été effectuée.
Les propriétés de l'en-tête sont spécifiées sous forme de paire nom-valeur qui sont séparées l'une de l'autre par un deux-points ':', (exemple nom:valeur)

# En-têtes :

**En-tête de requête :** est présent lorsque vous faites une requête au serveur, il contient des informations sur la requête telles que l'URL que vous avez demandée, la méthode (GET, POST, HEAD), le navigateur utilisé pour générer la requête et d'autres informations.

**Exemple**

```
User-Agent:”Mozilla/5.0 (Windows NT 10.0; WOW64; rv:41.0) Gecko/20100101 Firefox/41.0″
```

Le terme navigateur est également appelé user-agent. Ainsi, même une simple requête vers une page implique l'envoi d'informations sur votre navigateur et le système d'exploitation que vous utilisez. Vous pouvez voir dans le champ d'en-tête ci-dessus que nous utilisons Windows 10 et le navigateur Firefox 41.0.

**En-tête de réponse :** est envoyé depuis le serveur après que l'utilisateur a envoyé une demande pour une page ou une ressource particulière et il contient des informations telles que l'encodage utilisé dans le contenu, le logiciel serveur utilisé sur la machine serveur pour générer la réponse et d'autres informations.

**La plupart des sites cachent généralement les informations de leur serveur afin de rendre difficile pour les pirates de savoir quel logiciel est utilisé sur le serveur.**

### Ces ressources peuvent vous aider

En-tête HTTP

[https://code.tutsplus.com/tutorials/http-headers-for-dummies--net-8039](https://code.tutsplus.com/tutorials/http-headers-for-dummies--net-8039)
