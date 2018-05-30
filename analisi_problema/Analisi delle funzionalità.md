|FUNZIONALITÀ|TIPO|GRADO COMPLESSITÀ|
|------------|----|-----------------|
|REGISTRAZIONE|Memorizzazione dati, interazione esterno | semplice
|LOGIN|Interazione esterno,<br/>gestione dati |semplice
|CERCA PROFILO|Interazione esterno,<br/>gestione dati |media
|CERCA ANNUNCI|Interazione esterno,<br/>gestione dati |media
|GENSTIONE ANNUNCI|Interazione esterno,<br/>gestione dati,<br/>memorizzazione dati|complessa
|CREA ANNUNCIO|Interazione esterno,<br/>memorizzazione dati|semplice
|MODIFICA ANNUNCIO|Interazione esterno,<br/>gestione dati,<br/>memorizzazione dati|media
|CHIUDI ANNUNCIO|Interazione esterno,<br/>gestione dati|semplice
|GESTIONE PROFILO|Interazione esterno,<br/>gestione dati,<br/>memorizzazione dati|complessa
|LOGOUT|Interazione esterno|semplice
|MODIFICA INFO|Interazione esterno,<br/>gestione dati,<br/>memorizzazione dati|media
|NOTIFICA UTENTE|Interazione esterno,<br/>gestione dati|semplice
|AMMINISTRA PIATTAFORMA|Gestione dati,<br/>memorizzazione dati|complessa
|BANNA UTENTE|Gestione dati,<br/>memorizzazione dati|semplice
|ELIMINA ANNUNCIO|Gestione dati|semplice

### INFORMAZIONI/FLUSSO: REGISTRAZIONE
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Nome |semplice |Protezione media |Input |Non più di 40 caratteri |
|Cognome |semplice |Protezione media |Input |Non più di 40 caratteri |
|E-mail |semplice |Protezione molto alta |Input |Non più di 254 caratteri |
|Password |semplice |Protezione molto alta |Input |Non più di 50 caratteri |
|Telefono |semplice |Protezione alta |Input |Non più di 30 caratteri |
|Data di nascita |semplice |Protezione media |Input |Non più di 20 caratteri |
|Nome azienda |semplice |Protezione media |Input |Non più di 40 caratteri |
|Partita iva |semplice |Protezione media |Input |Non più di 20 caratteri |


### INFORMAZIONI/FLUSSO: LOGIN
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|E-mail |semplice |Protezione molto alta |Input |Non più di 254 caratteri |
|Password |semplice |Protezione molto alta |Input |Non più di 50 caratteri |


### INFORMAZIONI/FLUSSO: CERCA PROFILO
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Nome |semplice |Protezione media |Input |Non più di 40 caratteri |
|Cognome |semplice |Protezione media |Input |Non più di 40 caratteri |
|E-mail |semplice |Protezione molto alta |Input |Non più di 254 caratteri |
|Nome azienda |semplice |Protezione media |Input |Non più di 40 caratteri |


### INFORMAZIONI/FLUSSO: CERCA ANNUNCI
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Tipologia |composto |Protezione media |Input | |
|Zona |composto |Protezione media |Input | |
|Prezzo massimo |semplice |Protezione media |Input |Non più di 20 caratteri |
|Periodo disponibilità |composto |Protezione media |Input | |
|Caratteristiche affittuario |composto |Protezione media |Input | |


### INFORMAZIONI/FLUSSO: GESTIONE ANNUNCI
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Tipologia |composto |Protezione media |Input/Output | |
|Indirizzo |composto |Protezione media |Input/Output |Non più di 200 caratteri |
|Prezzo massimo |semplice |Protezione media |Input/Output |Non più di 20 caratteri |
|Periodo disponibilità |composto |Protezione media |Input/Output | |
|Caratteristiche affittuario |composto |Protezione media |Input/Output | |
|Note |semplice |Protazione media |Input/Output |Non più di 2000 caratteri |
|Foto |composto |Protazione media |Input/Output |Non più di 5MB c.da |



### INFORMAZIONI/FLUSSO: CREA ANNUNCIO
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Tipologia |composto |Protezione media |Input | |
|Indirizzo |composto |Protezione media |Input |Non più di 200 caratteri |
|Prezzo massimo |semplice |Protezione media |Input |Non più di 20 caratteri |
|Periodo disponibilità |composto |Protezione media |Input | |
|Caratteristiche affittuario |composto |Protezione media |Input | |
|Note |semplice |Protazione media |Input |Non più di 2000 caratteri |
|Foto |composto |Protazione media |Input |Non più di 5MB c.da |


### INFORMAZIONI/FLUSSO: MODIFICA ANNUNCIO
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Tipologia |composto |Protezione media |Input/Output | |
|Indirizzo |composto |Protezione media |Output | |
|Prezzo massimo |semplice |Protezione media |Input/Output |Non più di 20 caratteri |
|Periodo disponibilità |composto |Protezione media |Input/Output | |
|Caratteristiche affittuario |composto |Protezione media |Input/Output | |
|Note |semplice |Protazione media |Input/Output |Non più di 2000 caratteri |
|Foto |composto |Protazione media |Input/Output |Non più di 5MB c.da |



### INFORMAZIONI/FLUSSO: CHIUDI ANNUNCIO
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Tipologia |composto |Protezione media |Output | |
|Indirizzo |composto |Protezione media |Output | |
|Prezzo massimo |semplice |Protezione media |Output | |
|Periodo disponibilità |composto |Protezione media |Output | |
|Caratteristiche affittuario |composto |Protezione media |Output | |
|Note |semplice |Protazione media |Output | |


### INFORMAZIONI/FLUSSO: GESTIONE PROFILO
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Nome |semplice |Protezione media |Input/Output |Non più di 40 caratteri |
|Cognome |semplice |Protezione media |Input/Output |Non più di 40 caratteri |
|E-mail |semplice |Protezione molto alta |Input/Output |Non più di 254 caratteri |
|Password |semplice |Protezione molto alta |Input/Output |Non più di 50 caratteri |
|Telefono |semplice |Protezione alta |Input/Output |Non più di 30 caratteri |
|Data di nascita |semplice |Protezione media |Input/Output |Non più di 20 caratteri |
|Nome azienda |semplice |Protezione media |Input/Output |Non più di 40 caratteri |
|Partita iva |semplice |Protezione media |Input/Output |Non più di 20 caratteri |
|Contatti |composto |Protezione media |Input/Output | |



### INFORMAZIONI/FLUSSO: LOGOUT
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
| | | | | |



### INFORMAZIONI/FLUSSO: MODIFICA INFO
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Nome |semplice |Protezione media |Input/Output |Non più di 40 caratteri |
|Cognome |semplice |Protezione media |Input/Output |Non più di 40 caratteri |
|E-mail |semplice |Protezione molto alta |Input/Output |Non più di 254 caratteri |
|Password |semplice |Protezione molto alta |Input/Output |Non più di 50 caratteri |
|Telefono |semplice |Protezione alta |Input/Output |Non più di 30 caratteri |
|Data di nascita |semplice |Protezione media |Input/Output |Non più di 20 caratteri |
|Nome azienda |semplice |Protezione media |Input/Output |Non più di 40 caratteri |
|Partita iva |semplice |Protezione media |Input/Output |Non più di 20 caratteri |
|Contatti |composto |Protezione media |Input/Output | |



### INFORMAZIONI/FLUSSO: NOTIFICA UTENTE
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|Nome |semplice |Protezione media |Output | |
|E-mail |semplice |Protezione molto alta |Output | |
|Link Annuncio |semplice |Protezione media |Output | |


### INFORMAZIONI/FLUSSO: AMMINISTRAZIONE PIATTAFORMA
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|ID Annuncio |semplice |Protezione media |Input |Non più di 40 caratteri |
|Tipologia |composto |Protezione media |Output | |
|Indirizzo |composto |Protezione media |Output | |
|Prezzo massimo |semplice |Protezione media |Output | |
|Periodo disponibilità |composto |Protezione media |Output | |
|Caratteristiche affittuario |composto |Protezione media |Output | |
|Note |semplice |Protazione media |Output | | 
|ID Utente|semplice |Protezione molto alta |Output | |
|Nome |semplice |Protezione media |Output | |
|Cognome |semplice |Protezione media |Output ||
|E-mail |semplice |Protezione molto alta |Output | |
|Data di nascita |semplice |Protezione media |Output | |
|Nome azienda |semplice |Protezione media |Output | |
|E-mail admin |semplice |Protezione molto alta |Output | |
|Messaggio di avviso |semplice |Protezione media |Input |Non più di 1000 caratteri|
|Selagnazioni Utente |composto |Protezione media |Output | |



### INFORMAZIONI/FLUSSO: BANNA UTENTE
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|ID Utente|semplice |Protezione molto alta |Input |Non più di 40 caratteri |
|Messaggio di avviso |semplice |Protezione media |Input |Non più di 1000 caratteri|



### INFORMAZIONI/FLUSSO: ELIMINA ANNUNCIO
|INFORMAZIONE|TIPO|LIVELLO DI RISERVATEZZA|INPUT/OUTPUT|VINCOLI|
|------------|----|-----------------------|------------|-------|
|ID Annuncio |semplice |Protezione media |Output | |
|Messaggio di avviso |semplice |Protezione media |Input |Non più di 1000 caratteri|

