# Generatore di URL con Frammento di Testo

[ [English](README.md) | [Italiano](README.it.md) ]

Questo repository ospita un Bookmarklet JavaScript che consente agli utenti di generare URL con il Frammento di Testo Scroll-to direttamente dal loro browser. Selezionando del testo su una pagina web e cliccando sul bookmarklet, gli utenti possono creare un link che, quando visitato, scorre automaticamente fino al testo selezionato sulla pagina.

## Come Utilizzare

1. Crea un nuovo segnalibro nel tuo browser.
2. Copia e incolla il codice JavaScript fornito di seguito nella sezione URL del segnalibro.
3. Quando navighi, seleziona del testo su una pagina web che desideri collegare direttamente.
4. Clicca sul bookmarklet per generare un URL con il testo selezionato come Frammento di Testo Scroll-to.
5. Apparirà un prompt con l'URL generato. Copialo e usalo come necessario.

## Codice Bookmarklet

```javascript
javascript:(function(){var text=window.getSelection().toString();if(text){var baseUrl=window.location.href.split('#')[0];var formattedText=text.trim().replace(/ /g,'%20');var newUrl=baseUrl+'#:~:text='+formattedText;prompt('Copia questo URL:',newUrl);}else{alert('Seleziona del testo sulla pagina.');}})();
```

### Compatibilità

Questo bookmarklet si basa sulla funzionalità Frammento di Testo Scroll-to, che potrebbe non essere supportata da tutti i browser. Per informazioni dettagliate sulla compatibilità, si prega di fare riferimento a CanIUse: [URL Scroll-to-Text Fragment](https://caniuse.com/url-scroll-to-text-fragment).

### Licenza

Questo progetto è rilasciato sotto la Licenza MIT. Consulta il file LICENSE per maggiori dettagli.
