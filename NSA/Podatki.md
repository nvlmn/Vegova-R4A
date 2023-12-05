- Konstante — V C-ju \#define, v C++ const datatype name = value
	- define(“CONST1”, “123”);
	- echo CONST1;
- Spremenljivke
	- $val = 836;
	- echo $val;

	- Način navajanja
		- Numerične 
			- BIN: b010201
			- OCT: o324
			- HEX: xDEADBEEF
			- DEC: 718
		- Logične
		- Nizi
			- Običajni — “Teta Marta”
			- Numerični — “382”, “12e-3”, …

Je **case-sensitive jezik**, razen ko ni: npr. pri “True/true/TRUE”. 

Tipi
- NULL
- Array
- Object
- Resource

Avtomatična alokacija pomnilnika ob kreaciji, tip se določi sproti oz. je inferred. 

Da ugotoviš, katerega tipa je $var: 
```php
<?php 
	$x = 39238673783987393873982;

	//Tole je var_dump. Vrne tip in vrednost. Primeren je le za debug.
	var_dump($x); 
	// Vrne float, ker je zelo velik int in ga hrani z exponent notationom. 
?>
```

Za production uporabljamo funkcije:
- is_string()
- is_array()
- is_float()

Ampak te funkcije ti ne vrnejo True, če je $var tega tipa, ampak če se lahko converta v njega. 
Zato je A true in B false.

A: 
```php 
is_int(“273”);
```
B:
```php 
is_int(“lalala”);
```

#### Življenska doba podatka
- Od kracije do konca skripte **ALI**
- konca bloka kode (npr for loopa) ali
- ko jo na roke uničimo: 
```php
unset($var); 
```
- Če je spremenljivka nastavljena lahko prevermo z 
```php
isset($var); 
```
