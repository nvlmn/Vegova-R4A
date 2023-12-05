```php
class Tocka {
	public $x;
	public $y;
}

$t1 = new Tocka();
$t2 = new Tocka();
$t3 = new Tocka();

$tab = array(1, 2, 3w, 4, 5);
//Novodobno:
$tab1 = [1, 2, 3, 4, 5];
$tab2 = [‘z’,’Z’,’p’, 3];
```

Za pregled tabel
`echo var_dump($tab)` in `echo print_r($tab)`

```php
for($i = 0; $i < count($tab1); $i++)
	echo $tab1[$i] . “ ”;
```

#### Dodajanje elementov v tabelo, sprememba vrednosti
```php
$tab1[] = 65; // Zdaj nastane [1, 2, 3, 4, 5, 65]
$tab1[] = [’a’, ‘b’, ‘c’]; // Zdaj nastane [1, 2, 3, 4, 5, 65, [’a’, ‘b’, ‘c’]]
$tab1[7] = 0; // Kreacija, ko še ne obstaja
$tab1[7] = 33; // Ažuriranje že obstoječe vrednosti
$tab1[132] = ’wa’; // Zdaj nastane [1, 2, 3, 4, 5, 65, [’a’, ‘b’, ‘c’], 33, ‘wa’]
```

Identifikator in vrednost sta oba lahko predmet modifikacije — oboje si lahko izmislimo sami in nastavimo na poljubno vrednost. 

Če si identifikatorji sledijo se imenujejo indeksi. V tem primeru je to asociativna tabela.
Ko imamo identifikatorje, ki si ne sledijo, imajo luknjo, ali so alfanumerični med numeričnimi, je tabela asociativna. 

### Brisanje elementov
```php
// Za enostavne podatkovne tipe
$x = 3;
unset($x);

unset($tab1[6][1]);
// Zdaj nastane [1, 2, 3, 4, 5, 65, [‘b’, ‘c’], 33, ‘wa’]

unset($tab1[6]);
// Zdaj nastane [1, 2, 3, 4, 5, 65, 33, ‘wa’]
```

[[Tipi Tabel]]
[[Testni Podatki]]