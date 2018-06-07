## Piano del collaudo

Lato backend, sviluppo di Unit test (framework NUnit per .Net) per testare il funzionamento di ogni classe del controller e della persistenza.

Lato frontend, sviluppo di Unit test (framework Mocha per Javascript) per testare il funzionamento del codice responsabile dell'interattività lato browser della pagina web.

I test saranno scritti parallelamente al codice seguendo una metodologia di sviluppo Agile, favorita dal ristretto numero di membri nei Team di progettazione e sviluppo e dalla complessità dell'applicazione.




A	titolo d’esempio si riporta	solo il	test per la	classe Utente




[TestFixture]
public class TestUtente
{
	private Utente _utente;
	
[SetUp]
public void UtenteSetUp() {
	_utente = new Utente("Giovanni", "Mucciaccia", "gio@outlook.it","blablabla90", "blablabla90", 1234568978, new DateTime(1990,5,15) )
	}

[Test]
public void TestMethod() {
	Assert.That(_utente.getNome(), Is.EqualTo("Giovanni"));
	Assert.That(_utente.getCognome(), Is.EqualTo("Mucciaccia"));
	Assert.That(_utente.getEmail(), Is.EqualTo("gio@outlook.it"));
	Assert.That(_utente.getPassword(), Is.EqualTo("blablabla90"));
	Assert.That(_utente.getConfermaPassword(), Is.EqualTo("blablabla90"));
	Assert.That(_utente.getNumeroTelefono(), Is.EqualTo(1234568978));
	Assert.That(_utente.getDataNascita(), Is.EqualTo(new DateTime(1990,5,15)));
	}
	
[Test]
public void TestMethod() {
	_utente.setNumeroTelefono(1115478652);
	Assert.That(_utente.getNumeroTelefono(), Is.EqualTo(1115478652));
	}
}
