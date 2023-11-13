
## ESERCIZIO DI OGGI : Vite Yu-Gi-Oh
## nome repo: vite-yu-gi-oh

## DESCRIZIONE:
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Al caricamento della pagina, effettuate una chiama ajax all'API di Yu Gi Oh: https://db.ygoprodeck.com/api/v7/cardinfo.php
e con i dati restituiti, stampate una card per ogni carta.

- creazione progetto con Vite
- creazione componenti ( header, footer, main)
- in store.js variabile vuota `cards` per salvare dati chiamata axios
- in App.vue import di `store.js`
- in App.vue funzione `getCards` che fa chiamata axios a api e salva dati in `store.cards`
- in App.vue eseguire `getCards` in created()
- analizzare risposta con console log e salvare in `store.cards` soltanto la proprietà con le cards
- in AppMain.vue import di `store.js`
- v-for semplice di `store.cards` in AppMain.vue per vedere se ci sono dati (es: <div v-for="card in cards"> )
- usare un componente con props per le cards in AppMain.vue (es. <Cards v-for="(card, index) in cards" :item="card" />)

**ATTENZIONE**: l’api restituisce tutti i risultati in un colpo solo. Per evitare attese e/o rallentamenti nelle richieste, potete diminuire il numero di risultati sfruttando i parametri *num* e *offset*
https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0

## BONUS:
Creare un componente loader da visualizzare fintantoché i risultati non sono pronti.
