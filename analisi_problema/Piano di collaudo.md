## Piano del collaudo

Lato backend, sviluppo di Unit test (framework NUnit per .Net) per testare il funzionamento di ogni classe del controller e della persistenza.

Lato frontend, sviluppo di Unit test (framework Mocha per Javascript) per testare il funzionamento del codice responsabile dell'interattività lato browser della pagina web.

I test saranno scritti parallelamente al codice seguendo una metodologia di sviluppo Agile, favorita dal ristretto numero di membri nei Team di progettazione e sviluppo e dalla complessità dell'applicazione.

A titolo d’esempio si riporta solo il test per la classe Validator



```C#
	[TestFixture]	
	public class TestValidator
	{
	
		[Test]
		public void TestParse() {
			Assert.That(Validator.parse("Nome", "Giovanni"), true);
			Assert.That(Validator.parse("Email", "michele.rossi@unibo.it"), true);
			Assert.That(Validator.parse("Email", "michele.rossi.unibo.it"), false);
			Assert.That(Validator.parse("IVA", "ASDFGHJK123456"), false);
			Assert.That(Validator.parse("Birth", "11/10/1987"), true);
			Assert.That(Validator.parse("Password", "password"), false);
		}
	}
```
