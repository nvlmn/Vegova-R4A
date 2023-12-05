- Besedilni dokument
- Ima definirano strukturo
	- Enkapsulirana je od \<html> do \</html>.
	- Head
		- Pove brskalniku, kaj se doda dokumentu, kaj includa (npr .css, .js, …) in ostali meta-podarki kot so kodiranje.
		- V njem nastavimo ime, ki se bo pokazalo na zavihku (v \<title>)
		- Ikona zavihka se prenese iz korena strani, datoteka “favicon.ico”
	- Body
		- Vsebinski del

### XHTML
- Zahteva \<!DOCTYPE html>
- Imena značk so male črke
- Vse značke morajo biti zaprte
- Vrednosti atributov so vedno enkapsulirane — vse vrednosti pri k:v parih so v dvojnih narekovajih.
- Tage kot so img, br zaključimo z /:
	- \<img />
	- \<br />
- Tidy — validator za HTML, ki ti pove… kaj ni kul z njim

#### Delitev zaslona
- hr — horizontal ruler
- br — linebreak
- p
- div
- tabela — th (heading), td (data), tr (row)
- span — p/div, ki ne lomi vrstice oz. ne zavzame cele širine, ampak širino child elementa

#### CSS
- Stil — pojavnost elementov
- Vsebino (HTML) strogo ločimo od oblike (CSS).
- CSS1, CSS2 (obstaja CSS3)

#### Ziher bomo uporabljali
- Barve
- Pozicije
- Velikosti
- Hover (onhover animacije …)

### Vrste strani
- Statična stran
- Dinamična stran
	- Na strežniku ali
	- na odjemalcu
- Aplikacija
	- Načeloma več strani, ki povezano delujejo
		- Šibko povezane — podatke vedno zagotavljamo, ko se piše skripta, lahko se passajo argumenti (z POST/GET)
		- Močno povezane — na nivoju aplikacije je nekje flag, ki označuje katere strani aplikaciji pripadajo, **po navadi cookie-based**
[[HTML Forme]]
[[HTML Tabele]]