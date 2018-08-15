# Amélioration progressive

## Charger des fichiers suivant le navigateur

Voir :
- [The Slow Death of Internet Explorer and the Future of Progressive Enhancement](https://alistapart.com/article/the-slow-death-of-internet-explorer-and-future-of-progressive-enhancement)
- [Cutting the Mustard with Media Queries ](https://github.com/Fall-Back/CSS-Mustard-Cut)

### Charger un css suivant le navigateur

The following query will prevent the CSS file from being delivered to any version of Internet Explorer and older versions of other browsers:
```
<link id="mustardcut" rel="stylesheet" href="stylesheet.css" media="
  only screen,
  only all and (pointer: fine), only all and (pointer: coarse), only all and (pointer: none),
  min--moz-device-pixel-ratio:0) and (display-mode:browser), (min--moz-device-pixel-ratio:0)
">
```

### Charger un fichier js suivant le navigateur

This gives us one consistent dividing line between old and modern browsers:
```
(function() {
	var linkEl = document.getElementById('mustardcut');
	if (window.matchMedia && window.matchMedia(linkEl.media).matches) {
    	var script = document.createElement('script');
    	script.src = 'your-script.js';
    	script.async = true;
    	document.body.appendChild(script);
	}
})();
```

matchMedia brings the power of CSS media queries to JavaScript. The matches property is a boolean that reflects the result of the query. If the media query we defined in the link tag evaluates to true, the JavaScript file will be added to the page.

## Ressources
