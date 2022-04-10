<img src="images/readme/header-small.jpg" >

# G. Destructuring <!-- omit in toc -->

## Sommaire <!-- omit in toc -->
- [G.1. Principe du destructuring](#g1-principe-du-destructuring)
- [G.2. Destructuring et fonctions](#g2-destructuring-et-fonctions)
- [G.3. Mise en application](#g3-mise-en-application)

## G.1. Principe du destructuring
**Comme vu en cours, une des fonctionnalités ES6+ les plus utilisées s'appelle le "destructuring".**

Le destructuring permet de déclarer des variables dont les valeurs vont être remplies automatiquement par des propriétés d'objets. Prenons par exemple l'objet `character` ci-dessous :

```js
const character = { firstName: 'Skyler', lastName: 'White' };
```

Si l'on veut récupérer son nom et son prénom, sans le destructuring, on ferait ceci :
```js
const firstName = character.firstName,
	lastName = character.lastName;
```
**C'est assez verbeux** : on répète `character` deux fois, `firstName` deux fois et `lastName` deux fois également.

Et bien avec le destructuring on va pouvoir faire exactement la même chose mais en plus rapide :
```js
const { firstName, lastName } = character;
```

Notez les deux accolades autour du nom des constantes : c'est la syntaxe pour faire du desctructuring d'objets.

Notez que pour que ça marche, il faut que les constantes qu'on crée aient le même nom que les propriétés de l'objet qu'on destructure (même si un [système d'alias existe](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Op%C3%A9rateurs/Affecter_par_d%C3%A9composition#Affecter_avec_un_nom_diff%C3%A9rent)).

Le résultat, lui, est le même que dans l'exemple précédent : on crée deux constantes, dont les valeurs sont celles des propriétés de l'objet character.

**Notez bien que cela fonctionne pour les `const` mais bien entendu aussi pour les `let` !**

## G.2. Destructuring et fonctions
Le destructuring est souvent utilisé dans la déclaration de fonctions qui reçoivent des objets en paramètre. Par exemple, imaginons la fonction suivante :

```js
function kill(character) {
	console.log( `${character.firstName} ${character.lastName} is dead :'(` );
}
```

Le destructuring permet de simplifier l'écriture de la fonction :
```js
function kill({firstName, lastName}) {
	console.log( `${firstName} ${lastName} is dead :'(` );
}
```

Dans cette nouvelle version, le code est beaucoup moins verbeux, et surtout la fonction est maintenant quasiment **auto-documentée** : rien qu'en lisant la signature de la fonction, on sait que le paramètre qu'on doit lui passer est un objet (grâce aux accolades) et aussi qu'il doit avoir deux propriétés, firstName et lastName. Pratique !

## G.3. Mise en application
La consigne pour ce dernier exercice est simple : **appliquez le destructuring partout où c'est possible dans votre code !**


## TP suivant
[Pour accéder au TP suivant, cliquer ici](https://github.com/GuillaumeCar/react-tp2)
