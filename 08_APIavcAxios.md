# Chapitre : API PRATIQUE AVEC AXIOS


# Qu'est-ce qu'Axios ?

Axios est un client HTTP basé sur des promesses pour le navigateur et Node.js.
En utilisant Axios, il est facile d'envoyer des requêtes HTTP asynchrones aux points de terminaison REST et d'effectuer des opérations CRUD. La bibliothèque Axios peut être utilisée dans votre application JavaScript simple ou peut être utilisée avec des frameworks plus avancés comme React.js.
Il existe quelques différences entre axios et l'API Web Fetch :
Syntaxe : la requête http utilisant axios est plus simple que l'utilisation de fetch
Support : l'API Web Fetch n'est pas prise en charge par tous les navigateurs, par contre axios est pris en charge même par l'ancienne version du navigateur (comme IE)
Délai d'attente de réponse : la configuration du délai d'attente est beaucoup plus simple en utilisant axois qu'en utilisant l'API Fetch.

### Installer Axios

Pour installer axios, il suffit d'exécuter la commande suivante :

```
npm i axios
// or
npm install axios
```

# Utiliser Axios

La syntaxe d'Axios ressemble en grande partie à celle de l'API fetch.
Pour effectuer une requête get :

```
// Make a request for a user with a given ID
axios.get('/user?ID=12345')
 .then(function (response) {
   // handle success
   console.log(response);
 })
 .catch(function (error) {
   // handle error
   console.log(error);
 })
```

# Publication de données à l'aide d'Axios

La syntaxe de la requête post est la suivante :
`axios.post(url, data,config)`

* Url : l'url de l'api
* Données : les données à envoyer (champ facultatif)
* Config : la configuration de l'en-tête (champ facultatif)

```
axios
 .post("/user", {
   firstName: "Fred",
   lastName: "Flintstone"
 })
 .then(function(response) {
   console.log(response);
 })
 .catch(function(error) {
   console.log(error);
 });
```

# Demande de chaînage

Axios est livré avec une fonctionnalité intégrée qui nous donne la possibilité d'envoyer plusieurs requêtes.

```
const requestOne = axios.get("https://api.storyblok.com/v1/cdn/stories/health?version=published&token=wANpEQEsMYGOwLxwXQ76Ggtt");
const requestTwo = axios.get(https://api.storyblok.com/v1/cdn/datasources/?token=wANpEQEsMYGOwLxwXQ76Ggtt");
const requestThree = axios.get("https://api.storyblok.com/v1/cdn/stories/vue?version=published&token=wANpEQEsMYGOwLxwXQ76Ggtt");

axios
 .all([requestOne, requestTwo, requestThree])
 .then(axios.spread((firstResponse, secondResponse, thirdResponse) => {
     console.log(firstResponse.data,secondResponse.data, thirdResponse.data);
   })
 )
 .catch(errors => {
   console.error(errors);
 });
```

### Ces ressources peuvent vous aider

Requête POST avec React

[https://jasonwatmore.com/post/2020/02/01/react-fetch-http-post-request-examples](https://github.com/axios/axios#axiosposturl-data-config)
