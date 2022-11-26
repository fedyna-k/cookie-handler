# Cookie Handler

Une API de gestion de cookie simple pour le projet de dev web client-only.

1. [Create cookie](#create)
2. [Get cookies](#get)
3. [Remove cookie](#remove)
4. [Is cookie defined](#defined)
5. [Edit cookie](#edit)

<div id="create"></div>

## Create cookie

**Prototype** : ``createCookie (name, value, days=1);``

**Arguments**

|Nom|Type|Description|
|:-:|:-:|:-:|
|``name``|``string``|Le nom du cookie|
|``value``|``string``|Sa valeur|
|``days``|``number``|Le nombre de jours avant expiration|

**Renvoie**

Rien.

**Exemples d'utilisation**

```js
// Create cookie for 1 day
createCookie("myCookie", 42);
// Create cookie for a week
createCookie("weekCookie", "nice", 7);
```

<div id="get"></div>

## Get cookies

**Prototype** : ``getCookies ();``

**Arguments**

Aucun.

**Renvoie**

Un JSON contenant tout les cookies. Le JSON est de la forme ``{nom: valeur, ...}``

**Exemples d'utilisation**

```js
// Get all cookies
let cookies = getCookies();
```

<div id="remove"></div>

## Remove cookie

**Prototype** : ``removeCookie (...names);``

**Arguments**

|Nom|Type|Description|
|:-:|:-:|:-:|
|``names``|``...string``|Le ou les noms des cookies à supprimer|

**Renvoie**

Rien.

**Exemples d'utilisation**

```js
// Delete the cookie named "cookieToDelete"
removeCookie("cookieToDelete");
// Delete multiple cookies
removeCookie("cookie1", "cookie2", "cookie3");
```

<div id="defined"></div>

## Is cookie defined

**Prototype** : ``isCookieDefined (...names);``

**Arguments**

|Nom|Type|Description|
|:-:|:-:|:-:|
|``names``|``...string``|Le ou les noms des cookies à vérifier|

**Renvoie**

Un booléen indiquant si les cookies sont bien définis.

**Exemples d'utilisation**

```js
// Check the cookie named "cookieToTest"
isCookieDefined("cookieToTest");
// Check multiple cookies
isCookieDefined("cookie1", "cookie2", "cookie3");
```

<div id="edit"></div>

## Edit cookie

**Prototype** : ``editCookie (name, new_value);``

**Arguments**

|Nom|Type|Description|
|:-:|:-:|:-:|
|``name``|``string``|Le nom du cookie à modifier|
|``new_value``|``string``|Sa nouvelle valeur|

**Renvoie**

Un booléen indiquant si le cookie a pu être modifié.

**Exemples d'utilisation**

```js
// Edit cookie named "oldCookie"
editCookie("oldCookie", "Better value");
```
