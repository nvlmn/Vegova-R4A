- Komunikacija med ljudmi in računalniki
	- Komunikacija človek—računalnik (KČR) je študija o interakciji med ljudmi (uporabniki) in računalniki
	- V angleščini Human-Computer Interaction (HCI, ali Man-Machine Interaction \[MMI])
- Je presečišče računalniških znanosti, psihologije, ergonomije, inženirstva in grafičnega načrtovanja
- Je širok pojem, ki pokriva vse asprekte načinov na katere so ljudje v interakciji z računalniki
- Je disciplina, ki se ukvarja z načrtovanjem, vrednotenjem in implementacijo interaktivnih računalniških sistemov za človekovo uporabo in s šrudijami glavnih fenomenov, ki spremljajo te sisteme

- Ljudje za interakcijo z računalnikom uporabljajo uporabniški vmesnik (UV)
- Vmesnik (interface) je mesto kjer se srečujejo in delujejo neodvisni sistemi, ki med seboj lahko komunicirajo
- Uporabniški vmesnik (user interface) je mesto, ki združuje vhodne in izhodne naprave, programsko opremo in te resurse uporablja ter podpira:
	- Vhod omogoča uporabiku manipulacijo s sistemom
	- Izhod omogoča sistemu, da pokaže učinke uporabnikove manipulacije

### Vrste uporabniških vmesnikov
- Konzolno usmerjeni uporabniški vmesnik (Akcija -> Objekt)
	- **Navadni** tekstovni vmesniki
	- **Konzolni interaktivni** tekstovni vmesniki
- Grafično podprti uporabniški vmesniki (Objekt -> Akcija)
	- Dogodkovni interaktivni vmesnik (X11)
	- Dogodkovni interaktivni vmesnik z grafičnim uporabniškim vmesnikom (GUV)
		- Pišemo le kodo, ki pomeni odzive na dogodke
			- Odzivne funkcije (callbacks, message handlers) - npr. Qt
			- Poslušalci (listeners) - npr. Java

### Strukturne razlike UV
- Pri konzolnih vmesnikih programer aplikacije določa, kdaj bi prišlo do vnosa podatkov ali izpisa rezultatov. Govorimo o **postopkovnem programiranju** (procedural programming).
- Pri grafično podprtih uporabniških vmesnikih lahko uporabnik izvaja akcije kadarkoli. **Dogodkovno usmerjeno programiranje** (event-driven programming).
	- So načeloma bolj intuitivni
	- Zaporedja akcij ni mogoče vedeti v naprej
		- Klik miške, premik miške, pritisk na gumb, tipkanje, ...

### Navadni tekstovni vmesniki
- Niso interaktivni
- Linearno izvajanje
- V naprej določeno zaporedje akcij

### Konzolni interaktivni tekstovni vmesniki
- Vhodni ukazi uporabnika
- Nelinearno izvajanje
- Program se ustavi, ko čaka na vnos uporabnika in se nato nadaljuje
- Nepredvidljiv vrstni red akcij
- Veliko prostega časa

### Dogodkovni interaktivni vmesniki
- Vhodni ukaz uporabnika
- Nelineano izvajanje
- Uporabnik v vsakem trenutku lagko dela različne stvari (tipka v tekstovno okno, poveča okno, pritisne na tipko, kliče po grafičnem gradniku, ...)
- Tem odzivmo pravimo **dogodki = events**
- Nepredvidljiv vrstni red akcij
- Veliko prostega časa
- Zanka dogodkov, za katero poskrbi aplikacija sama, čaka na dogodke.
