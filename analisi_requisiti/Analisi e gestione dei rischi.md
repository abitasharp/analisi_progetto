
<b>TABELLA VALUTAZIONE DEI BENI</b>

BENE | VALORE | ESPOSIZIONE
-----|--------|------------
Sistema informativo | Alto. Supporto a tutta la gestione del sito. | Alta. Perdita di dati e immagine. Perdita finanziaria.     
Informazioni utente registrato | Alto. Dati personali dell'utente e preferenze riguardo i requisiti dell'annuncio | Alta. Perdita di immagine se venissero divulgati i dati personali dell'utente. Perdita finanziaria se venissero rubate le credenziali dell'utente.
Informazioni annuncio | Medio. Contiene tutte le informazioni relative agli annunci compreso il contatto del locatario e dettagli dell'inserzione (foto, zona,..). | Media. Perdita di immagine se l'annuncio che viene selezionato non è presente.

<b>TABELLA MINACCE/CONTROLLI</b>

MINACCIA | PROBABILITÀ | CONTROLLO | FATTIBILITÀ
---------|-------------|-----------|------------
Furto credenziali utente | Alta | Log di tutte le operazioni | Basso costo implementativo 
Furto credenziali amministratore | Alta | Password sicure obbligatorie, distribuite a personale ristretto. Log di tutte le operazioni | Basso costo implementativo
Intercettazione comunicazioni | Alta. Il sistema è distribuito client/server e avvengono molte interazioni fra i diversi nodi. | Cifratura delle comunicazioni | Il costo dipende dal tipo di cifratura scelta. Basso se è simmetrica, alto se simmetrica poichè richiede che un ente certificato rilasci una coppia di chiavi.
DoS | Bassa| Progettazione adeguata, controllo e limitazione degli accessi. | Basso costo. Impossibile prevedere un DoS.
Annunci malevoli | Alta | Il sistema deve controllare l'input utente | Basso costo, implementazione semplice.

<b>ANALISI TECNOLOGICA DELLA SICUREZZA</b>


TECNOLOGIA | VULNERABILITÀ
-----------|--------------
Autenticazione Username/Password | - Password banali <br/> - Utente rivela volontariamente la password <br/> - Utente rivela la password a causa di un attacco di Ingegneria Sociale
Cifratura comunicazioni  | Le vulnerabilità dipendono dal tipo di cifratura.<br/>Cifratura simmetrica:<br/> - Tempo di vita della chiave. Più informazioni cifrate con la stessa chiave, più materiale viene offerto per l'analisi del testo ad un attaccante.<br/> - Lunghezza della chiave<br/> - Memorizzazazione della chiave<br/> - Cifratura asimmetrica:<br/> - Memorizzazione della chiave privata
Archittettura client/server | - DoS<br/> - Man in the middle<br/> - Sniffing delle comunicazioni
Sito web | - Cross-site scripting

<b>REQUISITI DI PROTEZIONE DEI DATI</b>

Dall’analisi del rischio si possono evincere i seguenti ulteriori requisiti:

1. Creazione di un log per tracciare:
  a. tutte le azioni che avvengono sul sistema
  b. i messaggi scambiati tra le parti del sistema .

2. Individuare una corretta politica di controllo degli accessi.

3. I dati memorizzati e scambiati nel sistema devono essere protetti.

4. Deve essere possibile risalire alla paternità dei contenuti pubblicati nel sistema.
