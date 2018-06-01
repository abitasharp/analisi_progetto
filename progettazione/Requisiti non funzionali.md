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
