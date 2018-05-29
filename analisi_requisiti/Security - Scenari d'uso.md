| | |
|-|-|
TITOLO | **Controllo accesso** |
DESCRIZIONE | Gli accessi al sistema devono essere controllati|
MISUSE CASE |Sniffing informazioni, Furto credenziali|
RELAZIONI | |
PRECONDIZIONI |  L'attaccante ha i mezzi per scoprire e rubare almeno la mail di utenti/admin. |
POSTCONDIZIONI | Il sistema blocca momentaneamente l'accesso all'utente e notifica un tentativo di accesso fraudolento. |
SCENARIO PRINCIPALE | _-ATTACCANTE_<br/>Dopo aver scoperto alcune mail, tenta di accedere con un attacco a dizionario.<br/>_-SISTEMA_<br/>Controlla le credenziali immesse e blocca l'accesso nel caso risultino errate un numero fissato di volte.|
SCENARIO ATTACCO AVVENUTO CON SUCCESSO |_-ATTACCANTE_<br/> Attacco con dizionario riuscito. <br/>_-SISTEMA_<br/>  Il sistema controlla le credenziali e consente l'accesso, tenendone traccia nei log.|


| | |
|-|-|
TITOLO | **Garantire protezione** |
DESCRIZIONE | I dati devono essere protetti |
MISUSE CASE |Sniffing informazioni, Furto credenziali, Frode |
RELAZIONI | |
PRECONDIZIONI | a. L'attaccante ha i mezzi per intercettare i messaggi nel sistema<br/>b. L'attaccante ha i mezzi per modificare e spedire messaggi al destinatario|
POSTCONDIZIONI |Il sistema notifica un tentativo di frode |
SCENARIO PRINCIPALE |-_SISTEMA_ <br/>Il sistema si occupa di proteggere i messaggi tra le diverse parti.<br/>-_ATTACCANTE_<br/>Intercettazione messaggio nel sistema.<br/>Non riesce a rimuovere il meccanismo di protezione quindi ne genera uno e lo invia al destinatario.<br/>-_SISTEMA_<br/>Il sistema rivela che il messaggio non è pertinente e lo ignora.|
SCENARIO ATTACCO AVVENUTO CON SUCCESSO | -_SISTEMA_<br/>Il sistema si occupa di proteggere i messaggi nel sistema.<br/>-_ATTACCANTE_<br/>Intercettazione e rimozione meccanismo di sicurezza.<br/>Modifica del contenuto, riapplica il meccanismo e invia il messaggio al destinatario.<br/>-_SISTEMA_<br/>Il sistema elabora il messaggio e ne tiene traccia nei log.| 


| | |
|-|-|
TITOLO | **Non ripudio** |
DESCRIZIONE | La paternità e la validità delle dichiarazioni devono essere garantite|
MISUSE CASE | Frode|
RELAZIONI | |
PRECONDIZIONI | |
POSTCONDIZIONI |Il sistema rileva il tentativo di frode. |
SCENARIO PRINCIPALE | -_SISTEMA_<br/>Il sistema tiene traccia della paternità dei messaggi.<br/>-_ATTACCANTE_<br/>Generazione e invio di un messaggio al sistema.<br/>Negazione della transazione avvenuta<br/>-_SISTEMA_<br/>Il sistema riconosce la paternità della transazione e segnala il tentativo di frode.|
SCENARIO ATTACCO AVVENUTO CON SUCCESSO | -_SISTEMA_<br/>Il sistema tiene traccia della paternità dei messaggi.<br/>-_ATTACCANTE_<br/>Generazione e invio di un messaggio al sistema non riconducibile a lui.<br/>Negazione della transazione avenuta.<br/>-_SISTEMA_<br/>Il sistema elabora il messaggio e ne tiene traccia nei log.| 
