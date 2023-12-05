# Snov
[[Podatki]]
[[Nizi]]
[[Pseudotipi]]
[[CSS Positioning]]
[[Tabele]]
[[Organizacija Kode]]

Splošen interpretiran programski jezik, ki **je C-like**.

Dva načina uporabe:
- CLI (interaktiven shell, CLI interpreter)
- CGI (modul za HTTP strežnike, rezultat se izpiše v HTML)

Struktura kode (v .php datoteko zarinemo, po navadi nekam v body):
```php
<?php 
	phpinfo();
	
	// C-ctyle comment
	
	/*
	Multiline C-ctyle comment
	*/
	
	echo ’wowowowo’;
	print ’<h1>WOWOWOWOWO</h1>’;
?>
```

\\n je v CGI načinu izpizan kot “ ”.