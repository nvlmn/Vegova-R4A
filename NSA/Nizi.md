```php
$str = ‘1abc’; // Uporabimo, da lahko v njemu brez escapinga (\) navedemo dobule-qouted html parametre
$str = ”1abc”;
```

#binary-equals:
```php
a == b; // preveri če evaluira a in b v enako vrednost

a === b; // preveri tudi, če sta isti tip 
```

#### Relacije med nizi
- <, <=
- >, >=
- ==
- !=

Za sestavljanje večih nizov:
```php
$str = ”1a”.’bc’;
```

mb_strlen — da v stringu šteje tudi non-ASCII (po char, ne po sizeof(str)/sizeof(char)). mb = multi-byte.

Ekspliciten type-definition:

```php
$x = (int)322; // jeeej C-style
```

Izvajanje: 
- Von Neumann
	- Ukazi si sledijo top-to-bottom, razen če se zgodi vejite

