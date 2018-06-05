| | |
|-|-|
TITOLO | **Login** |
DESCRIZIONE | Permette di autenticarsi come utente registrato. |
ATTORI | Visitatore, Utente registrato |
RELAZIONI | Registrazione, Gestione annunci |
PRECONDIZIONI | |
POSTCONDIZIONI | |
SCENARIO PRINCIPALE | 1. L'utente inserisce le credenziali di accesso al sistema. <br/>2. Il sistema dopo le opportune verifiche presenta l'opportuna schermata iniziale.|
SCENARI ALTERNATIVI | A. Credenziali non riconosciute<br/>A.1. Il sistema dopo le opportune verifiche presenta nuovamente la schermata di accesso.|
REQUISITI NON FUNZIONALI | Protezione dei dati.|
PUNTI APERTI | |


| | |
|-|-|
TITOLO | **Registrazione** |
DESCRIZIONE | Il visitatore si registra sulla piattaforma |
ATTORI | Visitatore|
RELAZIONI | Login|
PRECONDIZIONI | |
POSTCONDIZIONI | I dati dell'utente vengono salvati|
SCENARIO PRINCIPALE | 1. Il visitatore accede alla sezione di registrazione. <br/>2. Il visitatore sceglie il tipo di profilo e inserisce i relativi dati di registrazione. <br/> 3. Il sistema memorizza i dati inseriti, valida l'email e invia una email contenente un link che permette di completare la procedura.<br/>4. Il sistema abilita l'account all'attivazione del link.|
SCENARI ALTERNATIVI | A. L'email inserita non è valida<br/>A.1. Il visitatore viene notificato e rediretto alla schermata di registrazione.<br/> B. La procedura non viene completata entro 24h (link non pervenuto) <br/>B.1. Il sistema elimina i dati inseriti annullando la registrazione.|
REQUISITI NON FUNZIONALI |Protezione di dati e privacy.<br/> Velocità di memorizzazione e semplicità d'uso.|
PUNTI APERTI |Proteggere la registrazione tramite test di Turing (es. CAPTCHA) al fine di impedirne l'uso improprio. |



| | |
|-|-|
TITOLO | **Gestione profilo**|
DESCRIZIONE | Permettere all'utente di interfacciarsi con i dati e preferenze inseriti nella registrazione|
ATTORI | Utente registrato|
RELAZIONI |Modifica profilo, Login, Logout |
PRECONDIZIONI |L'utente è registrato nella piattaforma. |
POSTCONDIZIONI | |
SCENARIO PRINCIPALE | 1. Login <br/> 2.L'utente accede alla schermata di gestione profilo. <br/>3.L'utente può visualizzare i dati e le preferenze inserite nella registrazione. <br/>4.L'utente può scegliere di modificare uno o più elementi del profilo. Il sistema lo reindirizza alla schermata aggiornata di gestione profilo.
SCENARI ALTERNATIVI | A. L'utente non è autenticato o la sessione è scaduta <br/> A.1. L'utente è rediretto alla schermata di login. |
REQUISITI NON FUNZIONALI | Protezione dei dati e privacy, semplicità d'uso. |
PUNTI APERTI | |




| | |
|-|-|
TITOLO | **Logout**|
DESCRIZIONE |Chiusura della sessione utente. |
ATTORI | Utente registrato|
RELAZIONI | Gestione profilo|
PRECONDIZIONI | L'utente è registrato nella piattaforma.|
POSTCONDIZIONI | La sessione è terminata.|
SCENARIO PRINCIPALE |1.L'utente si interfaccia con la gestione profilo.<br/> 2.L'utente sceglie di terminare la sessione.
SCENARI ALTERNATIVI | A.La sessione è già scaduta e l'utente cerca di fare il logout<br/> A.1.Il sistema notifica l'utente della disconnessione già avvenuta.|
REQUISITI NON FUNZIONALI | Protezione dei dati e semplicità d'uso. Velocità di operazione per l'accesso ai dati.  |
PUNTI APERTI | |




| | |
|-|-|
TITOLO | **Modifica Info**|
DESCRIZIONE | L'utente modifica uno o più elementi del profilo.|
ATTORI | Utente registrato |
RELAZIONI | Gestione profilo|
PRECONDIZIONI | L'utente è registrato sulla piattaforma.|
POSTCONDIZIONI | Il contenuto del profilo viene aggiornato. |
SCENARIO PRINCIPALE | 1. L'utente ha effettuato il login. <br/>2. L'utente va nella pagina di gestione profilo. <br/>3. L'utente modifica il contenuto di uno più campi (modificabili).<br/> 4. Il sistema notifica l'utente del successo dell'operazione e aggiorna il contenuto della pagina con le modifiche apportate. |
SCENARI ALTERNATIVI |A. L'utente non è autenticato o la sessione è scaduta<br/>A.1. L'utente è rediretto nella schermata di login. <br/> B. L'utente vuole modificare un contenuto non modificabile<br/>B.1. Il sistema notifica l'utente del fallimento dell'operazione.|
REQUISITI NON FUNZIONALI |Velocità delle operazioni di accesso ai dati. Protezione di dati e privacy e semplicità d'uso. <br/>Velocità di memorizzazione.  |
PUNTI APERTI | |






| | |
|-|-|
TITOLO | **Gestione annunci**|
DESCRIZIONE | Gestione di tutte le operazioni che l'utente registrato può effettuare sugli annunci.|
ATTORI | Utente registrato|
RELAZIONI | Crea annuncio, Chiudi annuncio, Modifica annuncio, Login|
PRECONDIZIONI | L'utente è registrato nella piattaforma|
POSTCONDIZIONI | |
SCENARIO PRINCIPALE | 1. Login<br/>2. L'utente accede alla schermata di gestione annunci. <br/>3. L'utente può scegliere di creare un annuncio. Il sistema lo reindirizza all'apposita schermata.<br/>4. L'utente può scegliere di modificare un annuncio aperto in precedenza. Il sistema lo reindirizza all'apposita schermata.<br/>5. L'utente può scegliere di chiudere un annuncio aperto in precedenza. |
SCENARI ALTERNATIVI | A. L'utente non è autenticato o la sessione è scaduta<br/> A.1. L'utente è rediretto alla schermata di login.|
REQUISITI NON FUNZIONALI | Velocità di ricerca dei dati e semplicità nella navigazione tra le diverse interfacce.|
PUNTI APERTI | |






| | |
|-|-|
TITOLO | **Crea annuncio**|
DESCRIZIONE | Permette all'utente di pubblicare un annuncio sulla piattaforma.|
ATTORI |Utente registrato |
RELAZIONI | Gestione annunci|
PRECONDIZIONI | L'utente è registrato nella piattaforma.|
POSTCONDIZIONI | L'annuncio è visibile sulla piattaforma.|
SCENARIO PRINCIPALE | 1. L'utente ha effettuato il login.<br/>2. L'utente va nella schermata di creazione annunci. <br/>3. L'utente inserisce i dati dell'annuncio.<br/> 4. L'utente eventualmente aggiunge delle restrizioni sugli affittuari e/o foto dell'immobile.<br/>5. L'utente conclude l'inserimento dei dati e il sistema pubblica l'annuncio sulla piatttaforma. |
SCENARI ALTERNATIVI | A. L'utente non è autenticato o la sessione è scaduta <br/>A.1. L'utente è rediretto alla schermata di login.<br/>B. L'utente non ha inserito tutti i dati obbligatori<br/>B.1. L'utente viene notificato dell'errore ed invitato ad inserire i dati mancanti. |
REQUISITI NON FUNZIONALI | Protezione dei dati, velocità delle operazioni di memorizzazione, semplicità d'uso.|
PUNTI APERTI |Proteggere l'operazione tramite test di Turing (es. CAPTCHA) al fine di impedirne l'uso improprio. |






| | |
|-|-|
TITOLO | **Cerca annunci**|
DESCRIZIONE |Permette di navigare tra gli annunci della piattaforma filtrandoli secondo vari criteri. |
ATTORI |Utente registrato, Visitatore  |
RELAZIONI | |
PRECONDIZIONI | |
POSTCONDIZIONI |Il sistema mostra tutti gli annunci compatibili con i filtri impostati.  |
SCENARIO PRINCIPALE | 1. L'utente inserisce i filtri di ricerca e naviga tra gli annunci compatibili. <br/>2. Se registrato, può salvare le preferenze dei filtri. <br/> 3. L'utente visualizza l'annuncio selezionato. |
SCENARI ALTERNATIVI | A. L'utente non ha effettuato il login e cerca di visualizare i contatti del locatario di un annuncio<br/>A.1. Il sistema reindirizza l'utente alla schermata di login.|
REQUISITI NON FUNZIONALI | Protezione dei dati, velocità delle operazioni di accesso ai dati, semplicità d'uso.|
PUNTI APERTI | |



| | |
|-|-|
TITOLO |**Chiudi annuncio** |
DESCRIZIONE | L'utente chiude l'annuncio rendendolo non più visibile nella piattaforma e disabilitando ulteriori modifiche.|
ATTORI | Utente registrato|
RELAZIONI | Gestione annunci |
PRECONDIZIONI | L'utente è registrato nella piattaforma ed ha pubblicato almeno un annuncio.|
POSTCONDIZIONI |L'annuncio selezionato non è più visibile nella piattaforma ma l'utente può vederlo nella propria cronologia. |
SCENARIO PRINCIPALE |1. L'utente ha effettuato il login. <br/>  2. L'utente va nella schermata di gestione annunci. <br/>3. L'utente sceglie un annuncio aperto e lo chiude. <br/>4. Il sistema notifica il successo dell'operazione.|
SCENARI ALTERNATIVI | A. L'utente non è autenticato o la sessione è scaduta <br/>A.1. L'utente è rediretto alla schermata di login.|
REQUISITI NON FUNZIONALI | Protezione dei dati, velocità delle operazioni di accesso ai dati, semplicità d'uso.|
PUNTI APERTI | |


| | |
|-|-|
TITOLO | **Modifica annuncio**|
DESCRIZIONE | L'utente modifica un annuncio precedentemente pubblicato. |
ATTORI |Utente registrato |
RELAZIONI | Gestione annunci|
PRECONDIZIONI | L'utente è registrato nella piattaforma ed ha pubblicato almeno un annuncio. |
POSTCONDIZIONI |Il contenuto dell'annuncio viene aggiornato.  |
SCENARIO PRINCIPALE | 1. L'utente ha effettuato il login.<br/>2. L'utente va nella schermata di gestione annunci.<br/>3. L'utente sceglie un annuncio aperto e lo modifica. <br/>4. Il sistema notifica il successo dell'operazione. |
SCENARI ALTERNATIVI | A. L'utente non è autenticato o la sessione è scaduta <br/>A.1. L'utente è rediretto alla schermata di login. |
REQUISITI NON FUNZIONALI | Protezione dei dati, velocità delle operazioni di accesso ai dati, semplicità d'uso.|
PUNTI APERTI | |




| | |
|-|-|
TITOLO | **Cerca profilo**|
DESCRIZIONE |Permette di effettuare una ricerca con eventuale aggiunta di filtri dei profili utente registrati sulla piattaforma. |
ATTORI |Utente registrato |
RELAZIONI |Login |
PRECONDIZIONI | L'utente è registrato sulla piattaforma. |
POSTCONDIZIONI |Il sistema mostra tutti i profili utente compatibili con i filtri impostati. |
SCENARIO PRINCIPALE | 1. L'utente si autentica eseguendo il login. <br/>2. L'utente inserisce i filtri di ricerca e naviga tra i profili mostrati dal sistema. <br/>3. L'utente visualizza il profilo selezionato.|
SCENARI ALTERNATIVI | A. L'utente non è autenticato o la sessione è scaduta <br/>A.1. L'utente è rediretto alla schermata di login.|
REQUISITI NON FUNZIONALI | Protezione dei dati, velocità delle operazioni di accesso ai dati, semplicità d'uso.|
PUNTI APERTI | |




| | |
|-|-|
TITOLO | **Notifica utente** |
DESCRIZIONE | Notifica l'utente privato alla pubblicazione di un annuncio comatibile con filtri di ricerca salvati. |
ATTORI | Nuovo annuncio compatibile  |
RELAZIONI | |
PRECONDIZIONI |L'utente è registrato come privato. <br/>L'utente ha salvato dei filtri di ricerca ed ha abilitato le notifiche.  |
POSTCONDIZIONI |L'utente riceve una email contenente un link dell'annuncio.  |
SCENARIO PRINCIPALE | 1. Si verifica l'evento 'Nuovo annuncio compatibile'.<br/>2. Il sistema seleziona tutti gli account privati  compatibili con l'annuncio in base ai filtri salvati <br/>3. Il sistema comunica tramite email dati e link dell'annuncio ad ognuno degli utenti selezionati.|
SCENARI ALTERNATIVI | |
REQUISITI NON FUNZIONALI |Protezione dei dati e della privacy. |
PUNTI APERTI | |




| | |
|-|-|
TITOLO |**Amministrazione Piattaforma** |
DESCRIZIONE |Permette all'Admin di gestire la lista degli utenti registrati e degli annunci pubblicati sulla piattaforma. |
ATTORI |Admin  |
RELAZIONI | Login, Banna Utente, Elimina Annuncio |
PRECONDIZIONI | L'Admin è registrato sulla piattaforma.  |
POSTCONDIZIONI | |
SCENARIO PRINCIPALE |1. Login.<br/> 2. L'Admin accede alla schermata di gestione della piattaforma. <br/>3. L'Admin può visualizzare la lista degli utenti registrati e degli annunci pubblicati. <br/> 4. L'Admin può scegliere di eliminare una o più voci dalle suddette liste. Il sistema lo reindirizza alla schermata corrispondente di ban utente o eliminazione annunci.|
SCENARI ALTERNATIVI |A. L'Admin non è autenticato o la sessione è scaduta <br/>A.1. L'Admin è rediretto alla schermata di login. |
REQUISITI NON FUNZIONALI |Protezione dei dati e della privacy, velocità delle operazioni di accesso ai dati. |
PUNTI APERTI | |




| | |
|-|-|
TITOLO | **Banna Utente**|
DESCRIZIONE | Permette all'Admin di rimuovere un utente dalla lista di utenti registrati sulla piattaforma memorizzandone i dati al fine di prevenire una nuova registrazione. |
ATTORI | Admin|
RELAZIONI |Amministrazione Piattaforma  |
PRECONDIZIONI | L'Admin è registrato sulla piattaforma. |
POSTCONDIZIONI |L'utente non può più effettuare il login e i suoi dati vengono salvati in una lista di utenti bannati.|
SCENARIO PRINCIPALE | 1. Login.<br/>2. L'admin si interfaccia con la schermata di amministrazione piattaforma.<br/>3. L'admin sceglie di bannare un utente. <br/>4. L'admin seleziona l'utente da bannare dalla lista di utenti registrati.|
SCENARI ALTERNATIVI | A. L'admin non ha effettuato il login o la sessione è scaduta. <br/>A.1. L'admin viene reindirizzato alla schermata di login.  |
REQUISITI NON FUNZIONALI | Protezione dei dati e della privacy, velocità delle operazioni di accesso ai dati. |
PUNTI APERTI | |





| | |
|-|-|
TITOLO | **Elimina Annuncio**|
DESCRIZIONE |Permette all'admin di rimuovere un annuncio dalla lista degli annunci pubblicati sulla piattaforma.  |
ATTORI |Admin |
RELAZIONI |Amministrazione piattaforma  |
PRECONDIZIONI | L'Admin è registrato sulla piattaforma.|
POSTCONDIZIONI |L'annuncio non è più visibile sulla piattaforma. |
SCENARIO PRINCIPALE |1. Login. <br/> 2. L'admin si interfaccia con la schermata di amministrazione piattaforma. <br/>3. L'admin sceglie di eliminare un annuncio.<br/>4. L'admin seleziona l'annuncio da eliminare dalla lista di annunci pubblicati.|
SCENARI ALTERNATIVI |A. L'admin non ha effettuato il login o la sessione è scaduta.<br/>A.1. L'admin viene reindirizzato alla schermata di login. |
REQUISITI NON FUNZIONALI |  Protezione dei dati e della privacy, velocità delle operazioni di accesso ai dati. |
PUNTI APERTI | |





| | |
|-|-|
TITOLO | **Cancella Profilo**|
DESCRIZIONE | Permette all'utente di rimuovere il proprio profilo, con dati annessi, dalla piattaforma. |
ATTORI |Utente registrato |
RELAZIONI |Gestione profilo |
PRECONDIZIONI |l'utente è registrato nella piattaforma. |
POSTCONDIZIOI |Tutti i dati relativi alla registrazione dell'utente vengono cancellati dal sistema. |
SCENARIO PRINCIPALE |1. L'utente accede alla pagina di Profilo. <br/> 2. L'utente sceglie di cancellare il proprio profilo. |
SCENARI ALTERNATIVI |A. L'utente non ha effettuato il login o la sessione è scaduta.<br/>A.1. L'utente viene reindirizzato alla schermata di login.  |
REQUISITI NON FUNZIONALI | Protezione dei dati e della privacy, velocità delle operazioni di accesso ai dati. |
PUNTI APERTI | |
