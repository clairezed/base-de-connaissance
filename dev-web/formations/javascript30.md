## 1. Drum Kit

[keycode.info](http://keycode.info) : pour trouver à quelle keyCode correspond quelle touche

**Gestion de l'audio et remise à zéro** pour relancer le son sans attendre la fin du son lancé.

```javascript
audio.currentTime = 0; // permet de faire rewind à start d'un fichier audio.
audio.play()
```

Pour faire un **TimeOut sur une transition css** (ex `transition: all .07s`), on peut écouter la fin de la transition d'un élément.

```javascript
// forEach nécessaire car on a une NodeList
keys.forEach(key => key.addEventListener('transitionend', myFunction));
```
Marche aussi avec `animationend`.
