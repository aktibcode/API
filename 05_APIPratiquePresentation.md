# Chapitre : API PRATIQUE - PRESENTATION


# Introduction

Depuis le début de ce cours, nous avons eu affaire à des données statiques, souvent codées en dur. Mais dans les applications réelles, nous devons extraire des données d'une ressource externe.
Que faire si nous voulons gérer des données à partir d'une API ? C'est le but de cette section.

Plus précisément, nous utiliserons l'API Fetch et axios comme exemples de demande et d'utilisation de données.

# Exemples d'API

ProgrammableWeb est un site qui répertorie plus de 15 500 API. Google Maps, Twitter, YouTube, Flickr et Amazon Product Advertising font partie des API les plus populaires. La liste suivante contient plusieurs exemples d'API populaires :

1. API Google Maps : les API Google Maps permettent aux développeurs d'intégrer Google Maps sur des pages Web à l'aide d'une interface JavaScript ou Flash. L'API Google Maps est conçue pour fonctionner sur les appareils mobiles et les navigateurs de bureau. Lien vers l'API : [Lien](https://cloud.google.com/maps-platform/)
2. API YouTube : les API de Google permettent aux développeurs d'intégrer des vidéos et des fonctionnalités YouTube dans des sites Web ou des applications. Elles incluent l'API YouTube Analytics, l'API YouTube Data, l'API YouTube Live Streaming, les API YouTube Player… lien vers l'API YouTube : [Lien](https://developers.google.com/youtube/)
3. API Flickr : l'API Flickr est utilisée par les développeurs pour accéder aux données de la communauté de partage de photos Flick. L'API Flickr se compose d'un ensemble de méthodes appelables et de certains points de terminaison d'API. Lien vers l'API : [Lien](https://www.flickr.com/services/api/)
4. API Twitter : Twitter propose deux API.
   * L'API REST permet aux développeurs d'accéder aux données principales de Twitter. [Lien](https://dev.twitter.com/)
   * L'API de recherche fournit des méthodes permettant aux développeurs d'interagir avec les données de recherche et de tendances de Twitter.Lien vers les API : [Lien](https://dev.twitter.com/)
5. Amazon Product Advertising API : L'API Amazon Product Advertising permet aux développeurs d'accéder à la fonctionnalité de sélection et de découverte de produits d'Amazon pour promouvoir les produits Amazon afin de monétiser un site Web. Lien vers l'API : [Lien](https://www.amazon.com/ap/signin?openid.return_to=https%3A%2F%2Faffiliate-program.amazon.com%2Fassoc_credentials%2Fhome&openid.identity=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.assoc_handle=amzn_associates_us&openid.mode=checkid_setup&marketPlaceId=ATVPDKIKX0DER&openid.claimed_id=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.ns=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0&openid.pape.max_auth_age=0)

# Qu'est-ce qu'une URL de base ?

![](https://i.imgur.com/zPWdLzT.png)

Une URL de base est essentiellement la partie cohérente de votre adresse Web.

Par exemple, vous remarquerez que la section d'adresse [https://www.google.com/](https://www.google.com/) apparaît toujours dans la barre d'adresse.

Il s'agit de l'URL de base. Tout ce qui la suit est appelé chemin d'URL.

Pour trouver l'URL de base de votre site Web, accédez à la page d'accueil du site. Ce que vous voyez dans la barre d'adresse de la page d'accueil de votre site est l'URL de base de votre site Web.

# L'exemple d'URL de base

Voici un exemple d’URL REST bien formée :

`https://284-RPR-133.mktorest.com/rest/v1/lead/318581.json?fields=email,firstName,lastName`

Qui est composé des parties suivantes :

**URL de base : **[https://284-RPR-133.mktorest.com/rest](https:)

**Chemin :** /v1/lead/

**Ressource :** 318582.json

**Paramètre de requête :** fields=email,firstName,lastName

Format API

[Ouvrir le lien](https://support.helpspot.com/index.php?pg=kb.page&id=162)
