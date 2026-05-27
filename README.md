# 🏔️ Simulatore Gestione Rifiuti per Rifugi Alpini 🏔️

**Descrizione**
Strumento e simulatore web progettato per la gestione e il monitoraggio dei rifiuti in quota. Questo progetto permette ai gestori di rifugi alpini di stimare volume e peso dei rifiuti prodotti durante una stagione operativa, ottimizzare i flussi di smaltimento e garantire la conformità normativa al D.Lgs. 152/2006.

---

## Funzionalità Implementate

### 1. Analisi e Stima della Produzione di Rifiuti
Il simulatore calcola automaticamente il carico di rifiuti in base ai parametri operativi inseriti:
*   **Configurazione Stagionale**: Impostazione del periodo stagionale, posti letto, tasso di occupazione e numero coperti ristorante.
*   **Flussi di Produzione**: Calcolo dinamico dei rifiuti generati da ospiti e escursionisti.
*   **Gestione "Grigliato"**: Calcolo specifico del rifiuto grigliato, con densità e volume distinti.

### 2. Gestione Composizione e Pre-Trattamento
Permette una modellazione granulare della tipologia di rifiuti:
*   **Composizione Dinamica**: Tabella configurabile per tipologia (Organico, Plastica, Vetro, ecc.).
*   **Simulazione Pre-Trattamento**: Opzione per attivare coefficienti di riduzione (volume e massa) per simulare l'uso di compattatori o sistemi di pre-trattamento prima dello stoccaggio finale.

### 3. Dashboard Operativa e Grafici
Visualizzazione immediata dei dati chiave tramite dashboard interattiva:
*   **KPI Principali**: Peso e Volume pre/post trattamento, con calcolo percentuale di efficienza dei trattamenti.
*   **Grafici Interattivi**:
    *   *Doughnut Chart*: Distribuzione percentuale dei rifiuti per tipologia.
    *   *Bar Chart*: Confronto visivo volumetrico tra rifiuti "grezzi" e compattati.
*   **Tabella Dettaglio**: Riepilogo per categoria con valori assoluti e percentuali.

### 4. Logistica e Analisi Costi
Ottimizzazione del trasporto in quota:
*   **Configurazione Mezzi**: Inserimento di parametri per Elicotteri, Droni, Teleferiche e Mezzi Terrestri (Payload, costi fissi, costi variabili per minuto).
*   **Ottimizzazione Viaggi**: Calcolo automatico del numero minimo di viaggi necessario per smaltire il totale dei rifiuti.
*   **Stima Costi**: Calcolo totale costo operativo e costo per kg smaltito per ogni mezzo disponibile.

### 5. Conformità Normativa (D.Lgs. 152/2006)
Modulo di controllo automatico per la conformità allo stoccaggio temporaneo:
*   **Monitoraggio Volumico**: Calcolo del giorno in cui si supera il limite di **30 m³** di stoccaggio.
*   **Monitoraggio Temporale**: Verifica rispetto al limite di giacenza massima (**90 giorni** / 3 mesi).
*   **Alert e Violazioni**: Evidenziazione visiva (segnali di allarme) in caso di superamento dei limiti di legge, indicando il "Giorno Critico" per lo svuotamento obbligatorio.

---

## Struttura del Progetto

Il file è monolitico (HTML + CSS + JS in uno) per semplicità di portabilità.

Layout a griglia con pannello di configurazione a sinistra e dashboard risultati a destra.

---

## Note per l'Utilizzo

1.  **Dati Predefiniti**: Il sistema include valori di default realistici per un rifugio alpino standard.
2.  **Validazione Input**: Controlli in tempo reale per evitare valori negativi o percentuali non coerenti (es. somma > 100%).
3.  **Privacy**: I dati vengono salvati localmente sul dispositivo dell'utente. Non vengono inviati a nessun server esterno.
