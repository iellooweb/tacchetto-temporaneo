# Tacchetto Service — anteprima del nuovo servizio

Anteprima statica per far vedere al cliente come apparirebbe il nuovo servizio
**Riparazione e Ricondizionamento impianti spina** all'interno del sito
[tacchettoservice.it](https://www.tacchettoservice.it).

**Anteprima online:** https://iellooweb.github.io/tacchetto-temporaneo/

> **Questo non è il sito del cliente.** È una copia di prova, ricostruita da zero
> in HTML e CSS per valutare una proposta. Il sito vero è un WordPress e non viene
> toccato finché la proposta non è approvata.

---

## Da dove iniziare

👉 **[`index.html`](index.html)** — la pagina di apertura: spiega cosa cambia e perché,
con gli schemi. È quella che si apre aprendo l'indirizzo dell'anteprima.

Da lì si raggiungono le due pagine ricostruite:

| Pagina | Cosa mostra |
|---|---|
| [`home.html`](home.html) | Home con la nuova card tra i servizi e la riga nel riquadro in alto |
| [`assistenza.html`](assistenza.html) | Pagina Assistenza con la nuova sezione dedicata al ricondizionamento |

Una fascia scura in cima a ogni pagina ricorda che si tratta di una bozza e
riporta alla pagina esplicativa.

---

## Cosa aspettarsi guardandola

- **I rettangoli grigi sono segnaposto.** Al loro posto, sul sito vero, ci sono già
  le foto: qui mancano semplicemente i file originali. Non fanno parte della proposta.
- **Il bordo giallo attorno alla nuova card è una segnalazione**, non grafica definitiva.
  Serve a far trovare le modifiche a colpo d'occhio e sparisce nella versione pubblicata.
- **I contenuti sono statici.** Il modulo contatti non invia niente, i link del menu
  verso pagine non incluse non portano da nessuna parte.

---

## Struttura

```
index.html        Spiegazione delle modifiche, con schemi — pagina di apertura
home.html         Replica della home con la nuova card
assistenza.html   Replica della pagina Assistenza con la nuova sezione
style.css         Foglio di stile condiviso dalle due pagine replica
img/              Le grafiche prima/dopo fornite dal cliente
robots.txt        Esclusione dai motori di ricerca
proposta.html     Reindirizzamento: conserva il primo indirizzo condiviso
```

`index.html` ha il proprio stile incorporato: non dipende da `style.css`,
così le modifiche alle pagine replica non possono romperla.

---

## Note tecniche

- HTML5 e CSS, nessun framework, nessuna compilazione: si apre anche facendo
  doppio clic sui file.
- Unica risorsa esterna: i caratteri Oswald e Barlow da Google Fonts.
- Responsive, con punti di rottura a 1080 / 960 / 720 px.
- Le animazioni di `proposta.html` rispettano l'impostazione di sistema
  "riduci movimento" e la pagina resta leggibile anche senza JavaScript.
- Tutte le pagine hanno `<meta name="robots" content="noindex">` e il repository
  include un `robots.txt`: l'anteprima non deve comparire nelle ricerche.

---

## Dopo l'approvazione

Questi file non vanno online: servono a decidere. A proposta approvata, le modifiche
vengono realizzate sul WordPress esistente (GeneratePress + GenerateBlocks) e da qui
si recuperano solo i testi e le scelte grafiche concordate.

Prima della pubblicazione sul sito vero vanno tolte la fascia "Demo" in cima alle
pagine e la segnalazione gialla attorno alla nuova card.
