# Epclise Bot

Bot WhatsApp multi-funzione (Baileys) con ~290 comandi/plugin.

## Owner
Numero owner: **393887347002**

## Installazione (locale o Quaxly / VPS)

```bash
npm install
```

## Avvio con Pairing Code (consigliato su server)

```bash
npm run code
# oppure
node epclise.js code
```

Il codice di pairing a 8 caratteri apparirà **direttamente nella console** del server.
Inseriscilo su WhatsApp > Dispositivi collegati > Collega con numero di telefono.

## Avvio con QR

```bash
npm run qr
```

## Avvio normale (dopo aver già fatto il pairing)

```bash
npm start
```

## Note per Quaxly / hosting
- Spazio disco: 1.5 GB è più che sufficiente.
- La cartella `EpcliseSession` deve essere persistente (non cancellarla al riavvio).
- Porta di default impostata a 3011 (puoi cambiarla in epclise.js).
- Node.js >= 20 consigliato.

## Struttura
- `epclise.js` → entry principale + pairing
- `index.js` → wrapper / cluster
- `config.js` → owner, nomi, API keys
- `handler.js` → gestione messaggi e plugin
- `plugins/` → tutti i comandi (~290 file)
- `lib/` → utility (sticker, canvas, store, ecc.)

## Comandi principali (esempi)
- Menu: `.menu` / `.help`
- Owner: comandi con prefisso OWNER_
- Admin gruppo: ADMIN_*, antilink, antispam, welcome, ecc.
- RPG / economy: molti plugin RPG-*
- Fun / sticker / download / AI / info

I comandi sono organizzati in file plugin separati. Puoi aggiungere/modificare/eliminare singoli file in `plugins/`.

## Personalizzazione
Modifica `config.js` per owner, nome bot, watermark, canali, API keys.

Buon uso!
