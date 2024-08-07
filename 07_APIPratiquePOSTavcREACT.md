# Chapitre : API PRATIQUE - POST AVEC REACT


# POSTEZ avec React.

L'API de récupération nous donne également la possibilité de publier des données sur l'API.

```
function postData() {
     // the function to post data to the api
     fetch("https://jsonplaceholder.typicode.com/users", {
       method: "POST", //setting the method
       headers: {
         Accept: "application/json",
         "Content-Type": "application/json"
       },//setting the header
       body: JSON.stringify(user)//setting the body
     })
       .then(res => res.json())
       .then(res => setData(res))
       .catch(err => setError(err));
   }
```

Dans l'exemple ci-dessus, nous allons ajouter un utilisateur dans l'API `"https://jsonplaceholder.typicode.com/users"`, nous allons utiliser la méthode Post

# POSTEZ avec React.

Dans ce code ci-dessous, nous avons ajouté une entrée pour le nom. Si nous cliquons sur Ajouter, cela ajoutera un utilisateur à l'intérieur de l'API.

```
const App = () => {
 const [user, setUser] = useState();
 const handleSubmit = e => {
   e.preventDefault();
   fetch("https://jsonplaceholder.typicode.com/users", {
     method: "POST",
     headers: {
       Accept: "application/json",
       "Content-Type": "application/json"
     },
     body: JSON.stringify(user)
   })
     .then(res => res.json())
     .then(res => console.log(res))
     .catch(err => console.log(err));
 };

 const handleChange = e =>
   setUser({ id: Date.now(), [e.target.name]: e.target.value });
 return (
   <div>
     <form onSubmit={handleSubmit}>
       <label>
         Person Name:
         <input type="text" name="name" onChange={handleChange} />
       </label>
       <button type="submit">Add</button>
     </form>
   </div>
 );
};
export default App;
```

![](https://i.imgur.com/gq2Nhf7.png)

### Ces ressources peuvent vous aider


Requête POST avec React

[https://jasonwatmore.com/post/2020/02/01/react-fetch-http-post-request-examples](https://jasonwatmore.com/post/2020/02/01/react-fetch-http-post-request-examples)

Lien vers l'exemple utilisé dans le cours

[https://codesandbox.io/s/fetching-data-from-api-i7leo](https://codesandbox.io/s/fetching-data-from-api-i7leo)
