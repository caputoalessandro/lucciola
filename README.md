# Lucciola 🪲

Una piccola luce per i momenti difficili, con una lucciola come mascotte. Stile da fiaba notturna: bosco scuro, luce d'ambra, foglie di ruggine.
Strumenti presi da terapia cognitivo-comportamentale (CBT), ACT, mindfulness (MBCT), DBT e logoterapia, un diario dell'umore che mostra che gli stati d'animo cambiano, e una scatola della speranza.
Funziona nel browser, si installa sulla schermata Home e funziona anche offline. I dati restano solo sul telefono.

> Lucciola non è un dispositivo medico, non fa diagnosi e non sostituisce un professionista. In caso di pericolo: 112.

## Cosa c'è dentro

| Sezione | Cosa fa |
|---|---|
| **Oggi** | «Sto male adesso» (2 domande → strumenti adatti), segna l'umore, piccolo passo in sospeso, «Questo passerà» |
| **Diario** | Curva dell'umore su 30 giorni, tutti i momenti segnati, pensieri smontati, lenti, passi |
| **Strumenti** | 17 strumenti con scheda: cos'è, quando usarlo, da quale libro viene |
| **Scatola** | Motivi, ricordi, persone (con numero), messaggi, foto; si apre a caso |
| **Aiuto** (rosso, in alto) | Numeri di emergenza, le tue persone, il piano di sicurezza |

## Fonti

Dai libri vengono solo i metodi; tutti i testi sono originali.

- David D. Burns, *Feeling Good*: distorsioni cognitive, tre colonne, doppio standard, previsione del piacere, piccoli passi
- Greenberger e Padesky, *Mind Over Mood*: registro dei pensieri, pensiero caldo, prove, pensiero equilibrato
- Russ Harris, *La trappola della felicità*: defusione, espansione, getta l'ancora, valori
- Williams, Teasdale, Segal, Kabat-Zinn, *The Mindful Way through Depression*: spazio di respiro in 3 passi, pensieri come eventi mentali
- Marsha M. Linehan, *Manuale DBT*: STOP, TIP, cinque sensi
- Viktor E. Frankl, *Uno psicologo nei Lager*: il senso, «chi ti aspetta»

## Lingue e paesi

- Interfaccia in **inglese** (predefinita) e **italiano**: si cambia nelle impostazioni o dal link nella presentazione. I testi stanno in `I18N.en` e `I18N.it` dentro `index.html`.
- La schermata **Aiuto** mostra numero di emergenza e linee di crisi del paese, scelto in automatico dal fuso orario (poi dalla lingua del telefono) o a mano nelle impostazioni.
- Paesi con numeri: Stati Uniti, Canada, Regno Unito, Irlanda, Australia, Nuova Zelanda, Italia, Germania, Austria, Svizzera, Francia, Spagna, Portogallo, Paesi Bassi, Belgio, Svezia, Norvegia, Danimarca, Finlandia, Polonia, Grecia, India, Giappone, Brasile, Messico, Sudafrica. Per gli altri: numero di emergenza e [findahelpline.com](https://findahelpline.com).
- I numeri sono nella costante `HELP`. **Verificali ogni tanto** (ultimo controllo: ottobre 2026): numeri e orari possono cambiare.

## Contenuto

| File | A cosa serve |
|---|---|
| `index.html` | L'app intera: contenuti, schermate, grafica |
| `manifest.webmanifest` | Nome, colori e icona per l'installazione |
| `sw.js` | Funzionamento offline |
| `icon-*.png` | Icone con la mascotte |
| `.nojekyll` | Dice a GitHub Pages di servire i file così come sono |

## Pubblicare un aggiornamento

1. Sostituisci `index.html` (e gli altri file cambiati) con la nuova versione: Add file → Upload files → Commit.
2. In `sw.js` cambia `VERSION` (per esempio da `lucciola-v1` a `lucciola-v2`), così i telefoni scaricano la versione nuova.
3. GitHub Pages aggiorna il sito in un paio di minuti: riapri l'app con la connessione attiva.

I dati restano salvati nel browser di ogni dispositivo e non vengono toccati dagli aggiornamenti.

## Backup

- **Automatico giornaliero** (attivo di default): alla prima apertura di ogni giorno l'app salva una copia dei dati in IndexedDB (`lucciola-backup`) e tiene le ultime 7. La copia del giorno non viene sovrascritta, quindi resta un punto di ritorno anche dopo «Cancella tutti i dati». Si ripristina da Impostazioni → I tuoi dati.
- **File giornaliero** (opzionale): i browser non permettono di salvare file da soli, quindi una volta al giorno la home mostra un promemoria con il pulsante «Salva file».
- **Manuale**: Esporta / Ripristina backup (file `.json`).

## Installare l'app

- iPhone: apri il sito in Safari → Condividi → "Aggiungi alla schermata Home".
- Android: apri il sito in Chrome → menu ⋮ → "Installa app".
