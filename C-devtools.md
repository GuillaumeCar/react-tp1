<img src="images/readme/header-small.jpg" >

# C. les devtools <!-- omit in toc -->

_**Lorsque l'on développe en JS, les outils de debug dont on dispose nous sont fournis par le navigateur. Tous les navigateurs (même Internet Explorer...) disposent d'outils de développement. Sur Chrome, pour les afficher c'est donc, comme vu plus haut, la touche <kbd>F12</kbd>. On peut également les afficher en faisant un clic droit dans la page et en cliquant sur "Inspecter l'élément".**_

### IMPORTANT !! <!-- omit in toc -->
**Pendant les TP gardez TOUJOURS les outils de développement (_et notamment la console_) ouverts, ça vous sauvera la vie !**


## Sommaire <!-- omit in toc -->
- [C.1. devtools : La console](#c1-devtools-la-console)
- [C.2. devtools : l'inspecteur d'éléments](#c2-devtools-linspecteur-déléments)
- [C.3. devtools : l'onglet Sources](#c3-devtools-longlet-sources)

## C.1. devtools : La console
La console sert à afficher les instructions `console.log()` mais aussi les erreurs éventuelles dans votre code (vous me direz que ce n'est pas la peine, que vous ne faites jamais d'erreur, mais on sait tous les deux que c'est un mensonge, *"n'est-ce pas ?"*).

<img src="images/readme/devtools-console.jpg" >

La méthode `console.log()` peut recevoir plusieurs paramètres, ils seront dans ce cas affichés les un après les autres, séparés par un espace. Remplacez le `console.log(...);` du `main.js` par :
```js
console.log('Welcome to ', {title:'REACTube', emoji: '📺'});
```

En fait l'objet `console` est un objet global qui contient la méthode `.log()` mais aussi d'autres méthodes qui permettent d'avoir un rendu différent et de filtrer les messages. Essayez les méthodes suivantes et constatez le résultat dans la console :
- console.warn()
- console.error()
- console.clear()

Enfin, la console permet de tester rapidement du code JS grâce à un champ de saisie. Tapez-y l'instruction `42+"12"-10` puis tapez <kbd>Entrée</kbd>. Le résultat s'affiche directement dans la console. Incroyable !

## C.2. devtools : l'inspecteur d'éléments

L'inspecteur d'éléments permet de consulter ET de manipuler le code HTML et CSS de la page.

<img src="images/readme/devtools-inspecteur.jpg" >

Il sera utile pour vérifier que le code HTML que va générer votre JS correspond bien à ce qui est attendu.

## C.3. devtools : l'onglet Sources
L'onglet sources permet d'inspecter le code JavaScript de la page, de placer des breakpoints et de stopper l'exécution du code quand une erreur survient. Quand l'exécution du JS est stoppée, on peut consulter les valeurs des variables locales et globales, de voir la call-stack, etc.

C'est probablement l'onglet des devtools le plus important lorsqu'on développe en JavaScript.

<img src="images/readme/devtools-sources.jpg" >

Pour l'utiliser, remplacez le contenu de votre fichier `main.js` en ajoutant le code suivant :
```js
let what = 'door';
console.log('Hold', 'the', what );
```
Rechargez la page, dans l'onglet "Sources" sélectionnez le fichier main.js (dans le panneau de gauche), puis cliquez sur le numéro de la 2e ligne. Une flèche bleue a du s'ajouter ce qui signifie qu'un breakpoint a été ajouté. Comme le code en question s'est déjà exécuté (puisque notre JS se lance au chargement de la page), rechargez la page pour que le breakpoint se déclenche.

Une fois la page rechargée, l'exécution est interrompue, et il est possible de voir à droite, dans l'onglet "Scope" les valeurs des variables locales et notamment de la variable `what`. Vous pouvez aussi consulter la valeur des variables au survol de la variable directement dans le code !

Pour reprendre l'exécution de la page, cliquez sur le bouton play bleu, puis re-cliquez sur le numéro de la 2e ligne pour enlever le breakpoint.

## Étape suivante <!-- omit in toc -->
Si tout fonctionne, vous pouvez passer à l'étape suivante : [D. Les chaînes de caractères](D-chaines.md)