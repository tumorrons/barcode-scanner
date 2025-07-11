# 🛒 Scanner & Database Prodotti

Un'app web progressiva (PWA) avanzata per scansionare codici a barre e gestire un database personale dei prodotti con prezzi, negozi e offerte.

## ✨ Caratteristiche Principali

### 📱 Scanner Avanzato
- **Scansione in tempo reale**: Rileva automaticamente i codici a barre
- **Ricerca nel database**: Verifica se il prodotto è già presente
- **Supporto multi-formato**: EAN, UPC, Code 128, Code 39, Code 93, Codabar e altri
- **Cambio fotocamera**: Alterna tra fotocamera frontale e posteriore

### 🗄️ Database Locale Completo
- **Gestione prodotti**: Nome, marca, categoria, descrizione
- **Prezzi multipli**: Aggiungi prezzi da diversi supermercati/negozi
- **Indicatore offerte**: Segna quando un prodotto è in offerta
- **Modifica e eliminazione**: Gestisci facilmente i tuoi prodotti
- **Ricerca avanzata**: Trova prodotti per nome, marca, codice o categoria

### 📊 Statistiche e Analytics
- **Contatori**: Totale prodotti e negozi nel database
- **Prezzo medio**: Calcolo automatico del prezzo medio
- **Visualizzazione organizzata**: Lista prodotti con tutte le informazioni

### 💾 Sistema di Backup Completo
- **Esportazione**: Scarica tutto il database in formato JSON
- **Importazione**: Carica backup precedenti con merge intelligente
- **Cancellazione sicura**: Opzione per resettare completamente il database
- **Compatibilità**: Backup compatibili tra dispositivi diversi

### 📱 Funzionalità Mobile
- **PWA installabile**: Funziona come app nativa
- **Interfaccia touch-friendly**: Ottimizzata per smartphone
- **Funzionamento offline**: Tutti i dati sono salvati localmente
- **Design responsivo**: Adattamento automatico a tutti gli schermi

## 🚀 Come Usare l'App

### Scansionare un Nuovo Prodotto
1. Apri il tab "📱 Scanner"
2. Premi "Avvia Scanner"
3. Inquadra il codice a barre del prodotto
4. Se il prodotto non è nel database, compila il form:
   - Nome prodotto (obbligatorio)
   - Categoria (alimentari, bevande, igiene, etc.)
   - Marca
   - Descrizione
   - Aggiungi uno o più prezzi con relativi negozi
   - Segna se è in offerta
5. Premi "Salva Prodotto"

### Gestire il Database
1. Vai nel tab "📊 Database"
2. Visualizza le statistiche generali
3. Usa la barra di ricerca per trovare prodotti
4. Modifica o elimina prodotti esistenti
5. Aggiungi nuovi prezzi ai prodotti esistenti

### Backup e Sicurezza
1. Tab "💾 Backup" per gestire i dati
2. **Esporta**: Scarica un file JSON con tutti i tuoi dati
3. **Importa**: Carica un backup precedente
4. **Merge intelligente**: I prodotti esistenti vengono aggiornati, quelli nuovi aggiunti

## 📊 Struttura Dati

Ogni prodotto nel database contiene:
```json
{
  "barcode": "1234567890123",
  "name": "Nome Prodotto",
  "category": "alimentari",
  "brand": "Marca",
  "description": "Descrizione opzionale",
  "prices": [
    {
      "store": "Supermercato A",
      "price": 2.50,
      "isOffer": false,
      "date": "2025-07-11T10:30:00.000Z"
    }
  ],
  "dateAdded": "2025-07-11T10:30:00.000Z",
  "lastModified": "2025-07-11T10:30:00.000Z"
}
```

## 🛠️ Installazione e Uso

### Installazione come PWA
**Android (Chrome):**
1. Apri l'app in Chrome
2. Menu (⋮) → "Aggiungi alla schermata Home"
3. Conferma l'installazione

**iOS (Safari):**
1. Apri l'app in Safari
2. Pulsante condivisione → "Aggiungi alla schermata Home"
3. Conferma l'installazione

### Requisiti Tecnici
- Browser moderno con supporto WebRTC
- Fotocamera del dispositivo
- JavaScript abilitato
- 5-10 MB di spazio di archiviazione locale

## 💡 Casi d'Uso Pratici

### 🛍️ Shopping Intelligente
- Scansiona prodotti mentre fai la spesa
- Confronta prezzi tra diversi supermercati
- Tieni traccia delle offerte migliori
- Evita di comprare prodotti che già possiedi

### 📈 Analisi Spesa
- Monitora i prezzi nel tempo
- Identifica i negozi più convenienti
- Traccia l'inflazione sui tuoi prodotti abituali
- Pianifica gli acquisti in base alle offerte

### 🏠 Gestione Casa
- Inventario della dispensa
- Scadenze prodotti (tramite descrizione)
- Lista della spesa intelligente
- Backup per condividere con la famiglia

## 🚀 Deployment su GitHub Pages

### Setup Iniziale
```bash
# 1. Crea repository su GitHub
# 2. Clona localmente
git clone https://github.com/tuonome/nome-repo.git
cd nome-repo

# 3. Aggiungi i file dell'app
# - index.html (app principale)
# - manifest.json (configurazione PWA)
# - sw.js (service worker)
# - README.md (documentazione)

# 4. Commit e push
git add .
git commit -m "Initial commit: Scanner & Database Prodotti"
git push origin main
```

### Attivazione GitHub Pages
1. Repository → Settings → Pages
2. Source: "Deploy from a branch"
3. Branch: "main" / Folder: "/ (root)"
4. Save
5. L'app sarà disponibile su: `https://tuonome.github.io/nome-repo`

## 🔧 Personalizzazione

### Aggiungere Nuove Categorie
Modifica l'array delle categorie in `index.html`:
```html
<select id="productCategory">
    <option value="nuova-categoria">Nuova Categoria</option>
    <!-- ... altre categorie ... -->
</select>
```

### Personalizzare il Design
Modifica le variabili CSS nel tag `<style>`:
```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #00ff88;
}
```

## 🔒 Privacy e Sicurezza

- **Dati locali**: Tutti i dati rimangono sul tuo dispositivo
- **Nessun server**: L'app funziona completamente offline
- **Backup criptati**: I file di backup sono in formato JSON leggibile
- **Controllo totale**: Puoi eliminare tutti i dati in qualsiasi momento

## 🐛 Risoluzione Problemi

### La fotocamera non funziona
- Verifica i permessi del browser
- Assicurati che l'app sia servita tramite HTTPS
- Prova a ricaricare la pagina
- Controlla se altri siti possono accedere alla fotocamera

### I codici non vengono rilevati
- Migliora l'illuminazione
- Mantieni il dispositivo stabile
- Pulisci l'obiettivo della fotocamera
- Prova a variare la distanza dal codice

### Problemi con il backup
- Controlla lo spazio disponibile sul dispositivo
- Verifica che il file JSON sia valido
- Prova a esportare prima di importare per test

### L'app non si installa come PWA
- Usa Chrome su Android o Safari su iOS
- Verifica che tutti i file siano caricati
- Controlla che manifest.json sia accessibile

## 🚀 Funzionalità Future

### Possibili Miglioramenti
- **Sincronizzazione cloud**: Google Drive, Dropbox integration
- **Condivisione famiglia**: Database condiviso tra dispositivi
- **Grafici prezzi**: Visualizzazione trend nel tempo
- **Notifiche offerte**: Alert quando un prodotto va in offerta
- **QR Code**: Supporto per codici QR
- **API prezzi**: Integrazione con servizi di confronto prezzi
- **Export CSV**: Esportazione in formato foglio di calcolo
- **Etichette**: Sistema di tag personalizzati
- **Geolocalizzazione**: Associa negozi alla posizione
- **Promemoria acquisti**: Sistema di reminder

## 📞 Supporto

### Debug e Troubleshooting
1. Apri Developer Tools (F12)
2. Controlla la console per errori
3. Verifica che tutti i file siano caricati
4. Testa su browser diversi

### Segnalazione Bug
- Descrivi il problema riscontrato
- Specifica browser e dispositivo usato
- Allega screenshot se possibile
- Includi eventuali messaggi di errore

## 📄 Licenza

Questo progetto è open source e può essere liberamente:
- Modificato per esigenze personali
- Distribuito e condiviso
- Usato per progetti commerciali
- Migliorato dalla community

---

**Inizia subito a catalogare i tuoi prodotti! 🛒📱**

*Un database personale ti aiuterà a fare acquisti più intelligenti e risparmiare denaro nel lungo termine.*