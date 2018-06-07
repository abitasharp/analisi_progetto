## Requisiti non funzionali

- Facile navigabilità delle schermate
- Tempo di risposta
- Sicurezza
- Protezione dei dati
- Non ripudio

Nello	specifico	caso	in	esame,	Usabilità	e	Sicurezza	hanno	pochi	conflitti	a	parte	l’eventuale	richiesta	di
un	ulteriore	login	se	per	caso	scade	la	sessione	di	lavoro.
Diversa	la	questione	che	riguarda	Tempo	di	risposta	e	Sicurezza/Protezione dei,	aggiungere meccanismi	di	cifratura per	migliorare
la	sicurezza	ovviamente	porta	ad	un	peggioramento	delle	prestazioni	del	sistema,
occorre	quindi	trovare	un	bilanciamento	tra	i	due	aspetti.
Considerando	la	tipologia	di	sistema	che	deve	essere	sviluppato,	si	ritiene	maggiormente	
critico	l’aspetto	di	sicurezza	dei	dati	in	quanto	le informazioni inserite dagli utenti nella registrazione
e negli annunci sono dati personali e vanno mantenuti criptati per evitare perdite nel caso in cui
un'attaccante riesca ad avere accesso ai record memorizzati nel DB.	Inoltre,	gli	utenti	principali	di	tale	sistema	sono umani	che	spesso	
non	sono	in	grado	di	percepire	se	il	Sistema	impiega	qualche	frazione	di	secondo	in	più	o	in	meno	nella	risposta,
non	si	hanno	vincoli	real-time	da	soddisfare.
Il non ripudio è garantito dall sicurezza del canale creato per la comunicazione tra utente e piattaforma.

## Scelta dell'architettura

Dal punto di vista architetturale, l’architettura più idonea per questo tipo di sistema è un’architettura client/server a quattro livelli:

- Client: Gli utenti interagiscono con la piattaforma tramite browser, questo permette un alto disaccoppiamento dall'hardware e grande portabilità.

- Proxy: È l'unico punto di accesso da internet, regola la comunicazione tra i server nella rete privata e i client esterni.

- Server: Si è scelto di utilizzare un unico server per tutte le operazioni svolte dalla piattaforma in quanto un'architettura distribuita oltre a rivelarsi più costosa in termini economici e progettuali, è stata ritenuta superflua poichè il traffico stimato (per il momento) non richiede soluzioni più sofisticate (load balancing ecc).

- DBMS: Per la gestione della  persistenza  si  avrà  un  server  dedicato che comunica con il server vero e proprio attraverso una rete privata e non esposta ad internet.

- Log: Per la gestione dei log  si  avrà  un  server  dedicato che comunica con il server vero e proprio attraverso una rete privata e non esposta ad internet.


- Map cache: Per ridurre il numero di richieste verso un server di mappe, si  avrà  un  server  responsabile di fare cache delle richieste più frequenti che comunica con il server vero e proprio attraverso una rete privata e non esposta ad internet.

Per garantire la sicurezza nella comunicazione client/server si è deciso di utilizzare il protocollo 
tls (transport layer security). TLS  è un protocollo crittografico che permette una comunicazione sicura dalla  sorgente  al  destinatario  (end-to-end)  su  reti TCP/IP fornendo autenticazione, integrità dei dati e cifratura.
Infine, per impedire attacchi di tipo Man-In-The-Middle è necessario registrare il proprio dominio presso CA (Certificate Authority).
