# Prezzo Netto

L'app **Prezzo Netto** è una Progressive Web App (PWA) il cui scopo è duplice: 
- velocizzare il recupero dei dati (percentuale di glassatura e prezzo al netto della glassatura).
- automatizzare il calcolo della tara totale (sacchetto + glassatura).

## 🚀 Funzionamento
Il flusso di utilizzo tipico è strutturato in questi passaggi:

1. **Selezionare il formato del sacchetto:** Si imposta il formato piccolo o grande (che corrispondono rispettivamente a 6g e 14g). Di default, per ogni nuovo PLU si autoimposta su "piccolo", essendo il più frequente.
2. **Inserire il PLU del prodotto:** Una volta inserito e premuto OK, si visualizza la descrizione dell'articolo. È possibile correggere l'immissione col tasto "CAMBIA PLU" senza perdere lo scontrino in corso.
3. **Inserire il peso lordo:** Il peso lordo deve essere inserito in *grammi* (es. `0,564 kg` diventa `564`). Anche qui è presente un tasto "CAMBIA PESO" in caso di errore. 
   > *Nota per i prodotti in promo:* viene mostrato il Prezzo Netto Promo, ma secondo le indicazioni va impostata solo la tara totale in cassa, non va fatta la forzatura del prezzo ai clienti con la card.
4. **Riepilogo Scontrino:** Dopo aver ottenuto la tara totale (sempre in grammi, per un rapido inserimento in cassa), cliccando su "INSERISCI NUOVO ARTICOLO" esso viene salvato nella sezione di riepilogo in basso. Questo conteggia anche automaticamente i sacchetti totali per poterli battere tutti insieme alla fine. 
   Cliccando "NUOVO SCONTRINO" in alto, la lista si azzera.

## 📱 Installazione
Trattandosi di una PWA, è possibile installarla sul tablet del punto vendita direttamente da **Google Chrome** (con altri browser non è garantito il funzionamento):

1. Aprire Chrome e recarsi all'indirizzo dell'app: [https://ljmele.github.io/prezzo_netto/](https://ljmele.github.io/prezzo_netto/)
2. Un popup potrebbe chiedere "Vuoi scaricare questa applicazione?". Premere **OK**.
   *(Se il messaggio non compare, aprire il menù di Chrome con i tre puntini in alto a destra e selezionare **Aggiungi a schermata Home**)*.
3. Scegliere sempre di **installare l'applicazione** piuttosto che creare un collegamento rapido, così l'app funzionerà correttamente anche se il tablet perde la connessione internet.
4. L'icona di Prezzo Netto apparirà tra quelle installate o nella Home.

## ⚙️ Prima Accensione e Sincronizzazione Database
Il database dell'app usa un file Excel che va precaricato con quello inviato dalla Sede:

1. Aprire l'app e cliccare sull'icona delle **impostazioni** in alto a destra.
2. Cliccare su **Sincronizza → File**.
3. Selezionare dal tablet (es. nella cartella Download) il file `Prezzi_fixed.xlsx` (scaricato in precedenza dall'email).
4. Apparirà un messaggio di conferma dell'importazione.
5. **Associazione PLU:** Per ogni PLU presente in vendita, selezionare dal menù a tendina il codice articolo esposto al momento. (I PLU non presenti nel proprio negozio vanno ignorati).
6. Cliccare su **SALVA** in alto a destra. Si consiglia di associare i codici un po' alla volta e salvare spesso per non perdere il lavoro.
7. Tornare alla schermata principale col tasto **HOME** in alto a sinistra.

## 🔄 Aggiornamento Codici Articolo
Nel caso alcuni codici articolo in negozio non siano nel file Excel fornito:

1. Creare una copia del file originale (es. nominandola `UD_Prezzi_fixed.xlsx`).
2. Aprire il file con **Microsoft Office** o **Google Sheets** (*Non usare Open Office per non rovinare l'estensione del file*).
3. Modificare il file aggiungendo o togliendo righe **senza toccare la formattazione della tabella** (non cambiare numero/nome delle colonne e non toccare le formule).
4. Salvare il file, trasferirlo sul tablet ed eseguire nuovamente la **Sincronizzazione** dalle impostazioni col nuovo file.
5. Aggiornare le associazioni PLU e assicurarsi che le vecchie associazioni non abbiano subito modifiche.

> **Importante:** Ricordarsi di aggiornare le associazioni PLU → Codice Articolo quando il codice articolo di un prodotto cambia in fase di messa in vendita. Segnalare eventuali errori nel file Excel di partenza alla Sede per farli correggere a monte.
