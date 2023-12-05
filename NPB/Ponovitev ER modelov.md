Je načrt podatkov, ki bodo na disku. 

## Ponovitev
#### Poznana razmerja
- 1:1, 
	- identifying,
	- non-identifying,
- 1:mnogo,  
	- identifying,
	- non-identifying,
- mnogo:mnogo (vedno identifying, vendo z vmesno tabelo).

Vsak entitetni tip ima atribute in entitetni identifikator (ki potem postane PK, ko se iz entitetnih tipov generira tabelo).

#### Primer rekurzivnih relacij
Narišite ER model, za hranjenje hierarhije podjetje (vodja, pomočnik).

- Podjetje (davcna - PK, naziv, naslov) ima 
- enega vodjo in več pomočnikov. 

- Hkrati zaposluje več delavcev, ki odgovarjajo pomočnikom. 

Želimo imeti evidenco — točno kateri delavec odgovarja kateremu pomočniku, pri čemer velja, da ima vsak pomočnik lahko podrejenih več delavcev. 

Pomočniki odgovarjajo vodji, vodja sam sebi. 

O vseh zaposlenih se hrani davčna, ime, priimek, izobrazba.