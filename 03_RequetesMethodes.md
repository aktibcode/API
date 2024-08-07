# Chapitre : REQUETES - METHODES


# Requetes

![](https://i.imgur.com/pqYaAp5.png)

Nous pouvons imaginer le navigateur Web comme le client et l’application informatique qui héberge un site Web comme le serveur.

**Exemple :** un client (navigateur) soumet une requête HTTP au serveur, puis le serveur renvoie une réponse au client.
La réponse contient des informations sur l'état de la requête et peut également contenir le contenu demandé.

# Méthodes

Les verbes HTTP les plus couramment utilisés (ou méthodes, comme on les appelle correctement) sont **POST** , **GET** , **PUT** , **PATCH** et **DELETE** . Ils correspondent aux opérations de création, de lecture, de mise à jour et de suppression (ou CRUD). Il existe également un certain nombre d'autres verbes, mais ils sont utilisés moins fréquemment. L'une de ces méthodes est OPTIONS et HEAD. Elles sont utilisées plus souvent que les autres.

<iframe allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/loNGJMMMD-A?list=PL-w_yrNy8uTaWNAYCFoyW0C0zPm4S9b3v"></iframe>

# POST

![](https://i.imgur.com/LMkbb5i.png)

La méthode POST est utilisée pour envoyer des données du client (navigateur) au serveur. Comme nous pouvons le voir dans l'exemple ci-dessous, nous avons utilisé Postman pour entrer l'URL 127.0.01 sur le port 3000 avec une méthode POST. Le corps de cette requête contient l'email et le mot de passe.

# GET

![](https://i.imgur.com/UNvkaIY.png)

Dans cet exemple, nous utilisons la méthode GET pour récupérer des données de l'API.

# PUT

**PUT** est utilisé pour mettre à jour les requêtes et modifier les entrées dans la base de données. Ainsi, les requêtes PUT sont généralement envoyées avec un ID en tant que requête ou paramètre et les nouvelles données sont affichées dans le corps.

```
//id as query
http://localhost:3000/user/profile/?id=5e3bebed40dfda2656da1788
//id as params
http://localhost:3000/user/profile/5e3bebed40dfda2656da1788
```

# PATCH

![](https://i.imgur.com/TAoEDv9.png)

La méthode de requête HTTP PATCH applique des modifications partielles à une ressource.
Contrairement à la méthode PUT qui permet uniquement le remplacement complet d'un document.

# DELETE

![](https://i.imgur.com/LTGlR2v.png)

Dans cet exemple, nous avons envoyé une demande de suppression de l'utilisateur et la méthode DELETE est utilisée avec l'ID `5e3bebed40dfda2656da1788`

# Conclusion

HTTP définit un ensemble de méthodes de requête qui indiquent l'action souhaitée à effectuer sur une ressource donnée. Même s'il peut s'agir de noms, ces méthodes de requête sont parfois appelées verbes HTTP. Vous pouvez consulter [https://www.w3schools.com/tags/ref_httpmethods.asp](https://www.w3schools.com/tags/ref_httpmethods.asp) .


Requête HTTP

[Ouvrir le lien](https://doc.4d.com/4Dv17/4D/17.4/HTTP-Request.301-4882428.fr.html#:~:text=La%20commande%20HTTP%20Request%20permet,la%20r%C3%A9ponse%20du%20serveur%20HTTP.&text=(*)%20Lors%20des%20requ%C3%AAtes%20https,r%C3%A9f%C3%A9rer%20%C3%A0%20la%20RFC%202732.)

Méthodes de requête HTTP

[Ouvrir le lien](https://rapidapi.com/blog/api-glossary/http-request-methods/)
