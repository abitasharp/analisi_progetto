| | |
|-|-|
TITOLO | **Controllo accesso** |
DESCRIZIONE | Gli accessi al sistema devono essere controllati|
MISUSE CASE |Sniffing informazioni, Furto credenziali|
RELAZIONI | |
PRECONDIZIONI |  L'attaccante ha i mezzi per scoprire e rubare almeno la mail di utenti/admin. |
POSTCONDIZIONI | Il sistema blocca momentaneamente l'accesso all'utente e notifica un tentativo di accesso fraudolento. |
SCENARIO PRINCIPALE | _-ATTACCANTE_  Dopo aver scoperto alcune mail, tenta di accedere con un attacco a dizionario.  _-SISTEMA_  Controlla le credenziali immesse e blocca l'accesso nel caso risultino errate un numero fissato di volte.|
SCENARIO ATTACCO AVVENUTO CON SUCCESSO |_-ATTACCANTE_   Attacco con dizionario riuscito.   _-STSREMA_    Il sistema controlla le credenziali e consente l'accesso, tenendone traccia nei log.|


| | |
|-|-|
TITOLO | **Garantire protezione** |
DESCRIZIONE | I dati devono essere protetti |
MISUSE CASE |Sniffing informazioni, Furto credenziali, Frode |
RELAZIONI | |
PRECONDIZIONI | a. L'attaccante ha i mezzi per intercettare i messaggi nel sistema  b. L'attaccante ha i mezzi per modificare e spedire messaggi al destinatario|
POSTCONDIZIONI |Il sistema notifica un tentativo di frode |
SCENARIO PRINCIPALE |-_SISTEMA_   Il sistema si occupa di proteggere i messaggi tra le diverse parti.  -_ATTACCANTE_  Intercettazione messaggio nel sistema.  Non riesce a rimuovere il meccanismo di protezione quindi ne genera uno e lo invia al destinatario.  -_SISTEMA_  Il sistema rivela che il messaggio non è pertinente e lo ignora.|
SCENARIO ATTACCO AVVENUTO CON SUCCESSO | -_SISTEMA_  Il sistema si occupa di proteggere i messaggi nel sistema.  -_ATTACCANTE_  Intercettazione e rimozione meccanismo di sicurezza.  Modifica del contenuto, riapplica il meccanismo e invia il messaggio al destinatario.  -_SISTEMA_  Il sistema elabora il messaggio e ne tiene traccia nei log.| 


| | |
|-|-|
TITOLO | **Non ripudio** |
DESCRIZIONE | La paternità e la validità delle dichiarazioni devono essere garantite|
MISUSE CASE | Frode|
RELAZIONI | |
PRECONDIZIONI | |
POSTCONDIZIONI |Il sistema rileva il tentativo di frode. |
SCENARIO PRINCIPALE | -_SISTEMA_  Il sistema tiene traccia della paternità dei messaggi.  -_ATTACCANTE_  Generazione e invio di un messaggio al sistema.  Negazione della transazione avvenuta  -_SISTEMA_  Il sistema riconosce la paternità della transazione e segnala il tentativo di frode.|
SCENARIO ATTACCO AVVENUTO CON SUCCESSO | -_SISTEMA_  Il sistema tiene traccia della paternità dei messaggi.  -_ATTACCANTE_  Generazione e invio di un messaggio al sistema non riconducibile a lui.  Negazione della transazione avenuta.  -_SISTEMA_  Il sistema elabora il messaggio e ne tiene traccia nei log.| 
