# Chapitre : API PRATIQUE - METHODE GET


# La requête GET avec les navigateurs

![](https://i.imgur.com/PN9MkEY.png)

Il est facile de faire une requête HTTP GET. Imaginons que vous souhaitiez visiter gomycode.co dans votre navigateur. Il vous suffit de lancer votre navigateur et de saisir l'adresse : [https://www.gomycode.co](https://www.gomycode.co/)

# Qu'est-ce que fetch ?

Pour récupérer des données à partir d'une API, nous pouvons utiliser la méthode fetch de JavaScript. Nous pouvons également utiliser une bibliothèque externe comme axios, request, superagent, supertest et bien d'autres.
Dans cette super compétence, nous allons utiliser la méthode fetch.

La méthode fetch est fournie par les API Web et elle est prise en charge par presque toutes les nouvelles versions de navigateur.

PS : Il n'est pas nécessaire d'installer quoi que ce soit.

Dans cette partie, nous allons obtenir la liste des cours de l'API algolia sur Redux.

```
"https://hn.algolia.com/api/v1/search?query=redux"
```

# La requête GET avec React.

Dans cette étape, nous allons créer notre projet React dans App.js. Ce dont nous aurons besoin est :

1. Un état pour définir les valeurs renvoyées par l'API.
2. Un état pour gérer l’erreur (s’il y en a).
3. utilisez le hook useEffect sur l'API après le montage du composant.

```
import React, { useEffect, useState } from "react";

const App = () => {
 const [data, setData] = useState();// where to store the returned data
 const [error, setError] = useState(null);// where to store the coming errors
 useEffect(() => {
   function fetchData() {// the function to fetch data from the api
     fetch("https://hn.algolia.com/api/v1/search?query=redux")
       .then(res => res.json())
       .then(res => setData(res))
       .catch(err => setError(err));
   }

   fetchData();
 }, []);
 return <div />;
};
export default App;
```

# La requête GET avec React.

Commençons par expliquer quelques concepts. Lorsque nous envoyons une requête à une API, il lui faudra un certain temps pour trouver les données nécessaires à partir de ses ressources et renvoyer exactement ce que nous voulons. Par conséquent, JavaScript ne bloquera pas le reste de l'opération mais continuera à exécuter le reste du programme et lorsque l'API nous donnera un résultat de notre requête, JavaScript le gérera alors. C'est l'approche asynchrone de JavaScript, nous la verrons plus en détail dans d'autres super-compétences.
Pour l'instant, JavaScript nous donne les `.then()` `.catch()`méthodes pour gérer les fonctions asynchrones.
En termes plus simples, lors de l'appel d'une API, nous indiquons au navigateur que la réponse prendra un certain temps pour qu'il puisse continuer son travail et il nous avertira lorsque la réponse reviendra.

```
function fetchData() {// the function to fetch data from the api
     fetch("https://hn.algolia.com/api/v1/search?query=redux")
       .then(res => res.json())// when the result comes back with success here is what to do
       .then(res => setData(res))
       .catch(err => setError(err));// if there is an error here what you have to do.
   }
```

# La requête GET avec React.

Si nous exécutons un console.log sur l'état des données, nous recevrons le résultat suivant :

![](https://i.imgur.com/vMD1mcb.png)

Il contient un tableau d'objets nommés hits. C'est ce que nous allons montrer aux utilisateurs.

# La requête GET avec React.

Si nous exécutons un console.log sur l'état des données, nous recevrons le résultat suivant :

```
import React, { useEffect, useState } from "react";

const App = () => {
 const [data, setData] = useState([]); // where to store the returned data
 const [error, setError] = useState(null); // where to store the coming errors
 useEffect(() => {
   function fetchData() {
     // the function to fetch data from the api
     fetch("https://hn.algolia.com/api/v1/search?query=redux")
       .then(res => res.json()) // when the result comes back with success here is what to do
       .then(res => setData(res.hits))
       .catch(err => setError(err)); // if there is an error here what you have to do.
   }

   fetchData();
 }, []);

 return (
   <div>
     <ul>
       {data.map(course => (
         <li>
           <a href={course.url}> {course.title}</a>
         </li>
       ))}
     </ul>
   </div>
 );
};
export default App;
```

### Sortir

![](https://i.imgur.com/8W9jmAT.png)

# La requête GET avec React : JSON

Si nous collons l'URL de l'API dans le navigateur, nous obtiendrons un résultat comme celui-ci :

![](https://i.imgur.com/pFmBSrO.png)

Cette représentation est appelée format JSON. C'est le résultat que l'API envoie à notre application.

# Qu'est-ce que JSON ?

JSON (JavaScript Object Notation) est le format de données le plus utilisé pour l'échange de données sur le Web. Cet échange de données peut avoir lieu entre deux applications informatiques situées à des emplacements géographiques différents ou exécutées sur la même machine.

L'avantage est que JSON est un format compréhensible aussi bien par les humains que par les machines. Ainsi, même si les applications/bibliothèques peuvent analyser les données JSON, les humains peuvent également les consulter et en déduire un sens.
Un document JSON peut contenir du texte, des accolades, des crochets, des deux points, des virgules, des guillemets et peut-être quelques autres caractères.

Principalement, JSON repose sur deux structures :

1. Une collection de paires nom/valeur. Dans divers langages, cela se présente sous la forme d'un objet, d'un enregistrement, d'une structure, d'un dictionnaire, d'une table de hachage, d'une liste à clés ou d'un tableau associatif.
2. Une liste ordonnée de valeurs. Dans la plupart des langages, elle est réalisée sous la forme d'un tableau, d'un vecteur, d'une liste ou d'une séquence.

![](https://i.imgur.com/pFmBSrO.png)

### Ces ressources peuvent vous aider


Récupérer des données avec React.

[https://reactjs.org/docs/faq-ajax.html#how-can-i-make-an-ajax-call](https://reactjs.org/docs/faq-ajax.html#how-can-i-make-an-ajax-call)

Récupérer des données à l'aide de modèles dans React.

[https://blog.logrocket.com/patterns-for-data-fetching-in-react-981ced7e5c56/](https://blog.logrocket.com/patterns-for-data-fetching-in-react-981ced7e5c56/)
