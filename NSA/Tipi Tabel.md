
- indeksne (1, 2, 3, 4, …)
- asociativne (key=value pair recimo “ime”=“marko”)

#### Operacije nad indeksi
- unset
- \[] — dodajanje
- \[x] — pisanje na ineks `x`

### Podajanje spremenljivk kot del URL-ja
Uporabljamo tabelo `$_GET`. Če gremo npr. na URL http://localhost/stran.php?x=2&y=3 se vrednosti x=2 in y=3 dodata v to tabelo. 

##### Primer uporabe
```php
echo 
	“X: ” . 
	$_GET[”x”] . 
	
	“Y: “ . 
	$_GET[”y”];
```

##### Tabela, s katero bomo manipulirali:
|ime|priimek|naslov|telefon|rojstvo|
|-|-|-|-|-|
|Leopold|Novački|Vegova 4|01-213-4567|2000|
|Lea|Novački|Vegova 4|01-213-4568|2005|

##### Zapišemo kot asociativno tabelo v PHP:
```php
$oseba = [
	‘ime’ => ‘Leopold’,
	‘priimek’ => ‘Novački’,
	‘naslov’ => ‘Vegova 4’,
	‘telefon’ => ‘01-213-4567’,
	‘rojstvo’ => ’2000’
];

$oseba1 = [
	‘ime’ => ‘Lea’,
	‘priimek’ => ‘Novački’,
	‘naslov’ => ‘Vegova 4’,
	‘telefon’ => ‘01-213-4568’,
	‘rojstvo’ => ’2005’
];

print_r($oseba);

// Naredimo lahko tabelo tabel (tabelo oseb):
$osebe = [];
$osebe[] = $osebe;
$osebe[] = $osebe1;

print_r($oseba);

// Še ena opcija, ki jih prenese na “named” polja, imenovana po imenu osebe, ne le indexed (0 in 1)
$osebe = [];
$osebe[$oseba[”ime”]] = $oseba;
$osebe[$oseba1[”ime”]] = $oseba1;


// S Classom
class Obseba {
	private $ime;
	private $priimek;
	private $naslov;
	private $telefon;
	private $rojstvo;

	public function get_ime() // getIme je bolj C-style
	{
		return $this->ime;
	}
	
	// Uporaba konstruktorja (nov način):
	function __construct(…$z) {
		$this->ime = $z[0];
		$this->priimek = $z[1];
		$this->naslov = $z[2];
		$this->telefon = $z[3];
		$this->rojen = $z[4];
	}
}

$os = new Oseba(‘Janez’, ‘Novak’, ...);

echo “Ime: “ . $os->get_ime();
```

Asociativni način: obravnava ključe.
- Tudi ==ključ je podatek==, ne le vrednost
