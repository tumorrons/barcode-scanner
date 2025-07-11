# 📱 Scanner Codici a Barre

Un'app web progressiva (PWA) per scansionare codici a barre utilizzando la fotocamera del dispositivo mobile.

## ✨ Caratteristiche

- **Scansione in tempo reale**: Legge automaticamente i codici a barre inquadrati
- **Supporto multi-formato**: EAN, UPC, Code 128, Code 39, Code 93, Codabar e altri
- **Interfaccia mobile-first**: Ottimizzata per smartphone e tablet
- **Cronologia scansioni**: Mantiene un registro delle ultime 10 scansioni
- **Copia negli appunti**: Funzione per copiare rapidamente i codici
- **Cambio fotocamera**: Possibilità di alternare tra fotocamera frontale e posteriore
- **PWA**: Installabile come app nativa sul dispositivo
- **Funziona offline**: Utilizzo anche senza connessione internet

## 🚀 Come usare

1. Apri l'app nel browser del tuo dispositivo mobile
2. Premi "Avvia Scanner" per attivare la fotocamera
3. Inquadra un codice a barre con la fotocamera
4. Il codice verrà automaticamente rilevato e mostrato
5. Utilizza "Copia" per copiare il codice negli appunti

## 🔧 Installazione su dispositivo

### Android (Chrome)
1. Apri l'app in Chrome
2. Tocca i tre punti in alto a destra
3. Seleziona "Aggiungi alla schermata Home"
4. Conferma l'installazione

### iOS (Safari)
1. Apri l'app in Safari
2. Tocca l'icona di condivisione (quadrato con freccia)
3. Seleziona "Aggiungi alla schermata Home"
4. Conferma l'installazione

## 📱 Requisiti

- Browser moderno con supporto per:
  - WebRTC (accesso alla fotocamera)
  - Service Workers (per PWA)
  - Canvas API (per elaborazione immagini)
- Fotocamera del dispositivo
- Connessione internet (solo per primo caricamento)

## 🛠️ Tecnologie utilizzate

- **HTML5**: Struttura dell'app
- **CSS3**: Styling con design glassmorphism
- **JavaScript (ES6+)**: Logica dell'applicazione
- **QuaggaJS**: Libreria per la lettura di codici a barre
- **Web APIs**: MediaDevices, Canvas, Clipboard
- **Service Workers**: Per funzionalità offline e PWA

## 📂 Struttura file

```
barcode-scanner/
├── index.html          # File principale dell'app
├── manifest.json       # Configurazione PWA
├── sw.js              # Service Worker
└── README.md          # Questo file
```

## 🌐 Come caricare su GitHub

1. Crea un nuovo repository su GitHub
2. Carica questi file:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `README.md`
3. Vai nelle impostazioni del repository
4. Scorri fino a "Pages"
5. Seleziona "Deploy from a branch"
6. Scegli "main" branch
7. La tua app sarà disponibile su `https://tuonome.github.io/nome-repository`

## 🔒 Privacy e sicurezza

- L'app funziona completamente lato client
- Nessun dato viene inviato a server esterni
- Le scansioni sono salvate solo localmente sul dispositivo
- La fotocamera è utilizzata solo per la scansione, senza registrazioni

## 🐛 Risoluzione problemi

### La fotocamera non si attiva
- Controlla i permessi del browser per la fotocamera
- Assicurati che l'app sia servita tramite HTTPS
- Prova a ricaricare la pagina

### Codici non rilevati
- Assicurati che il codice sia ben illuminato
- Mantieni il dispositivo stabile durante la scansione
- Prova a variare la distanza dal codice

### App non installabile
- Controlla che il browser supporti le PWA
- Verifica che tutti i file siano caricati cor