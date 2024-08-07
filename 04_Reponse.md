# Chapitre : REPONSE


# Réponse : Introduction

![](https://i.imgur.com/7Z3WTjD.png)

**La réponse HTTP** est le paquet d'informations envoyé par le serveur au client en réponse à une requête antérieure (GET, POST, PUT…) émise par un client. Une réponse HTTP contient les informations demandées par le client.

# Statut

Les codes d'état de réponse HTTP indiquent si une requête HTTP spécifique a été exécutée avec succès ou non. Les réponses sont regroupées en cinq classes :

1. Réponses informatives (100–199),
2. Réponses réussies (200–299),
3. Redirections (300–399),
4. Erreurs client (400–499),
5. Erreurs de serveur (500–599).

### ***Quel est le but des codes d’état HTTP ?***

Les codes d'état HTTP sont des codes de réponse standard fournis par les serveurs de sites Web sur Internet. Les codes permettent d'identifier la cause du problème lorsqu'une page Web ou une autre ressource ne se charge pas correctement.

# Statut : exemple

### **Description de l'état de la réponse HTTP :**

L'élément Status-Code dans une réponse de serveur est un entier à 3 chiffres où le premier chiffre du Status-Code définit la classe de réponse et les deux derniers chiffres n'ont aucun rôle de catégorisation. Il existe 5 valeurs pour le premier chiffre. Voici un tableau décrivant la valeur de statut existante.

![](https://i.imgur.com/HzIlaCL.png)

### Dans le tableau ci-dessous, nous retrouvons le statut de réponse le plus utilisé.

![](https://i.imgur.com/Q6flEbI.png)

# Corps

![](https://i.imgur.com/x0Yy5sL.png)

Un message HTTP se compose d'un en-tête de message et d'un corps de message facultatif, séparés par une ligne vide, comme illustré ci-dessus.

# Corps

**Le corps de la réponse** contient les données de ressource demandées par le client.

Dans l'exemple ci-dessous, les données météorologiques ont été demandées à la ville d'Hyderabad. Si nous examinons le corps de la réponse, il contient les informations météorologiques de la ville. Il contient également des informations sur la température, l'humidité, la description de la météo et d'autres propriétés météorologiques de la ville.

```
Response Body:

{
   "City": "Hyderabad",
   "Temperature": "25.7 Degree celsius",
   "Humidity": "51 Percent",
   "WeatherDescription": "haze",
   "WindSpeed": "2.6 Km per hour",
   "WindDirectionDegree": "120 Degree"
}
```

Pour résumer, une API doit spécifier les réponses pour toutes les opérations d'API. Chaque opération doit avoir au moins une réponse définie et il s'agit généralement d'une réponse réussie. Une réponse est définie par son code d'état HTTP et les données renvoyées dans le corps et/ou les en-têtes de la réponse.

Réponse HTTP

[Ouvrir le lien](https://www.w3.org/Protocols/rfc2616/rfc2616-sec6.html)
