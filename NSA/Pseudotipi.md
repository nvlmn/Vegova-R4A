```php
function vsota($a, $b) {
	return $a + $b;
}
```
za 1 in 3 = 4, deluje
za “1” in 3 = 4, deluje
za ‘1Afna’ in 3 = /, ne deluje
za “1Afna” in 3 = 4, deluje
	ampak dobimo warning, ker splica string

Za cela do limita int tipa:
```php
function vsota(int $a, int $b) : int {
	return $a + $b;
}
```

Za cela, a tudi tista, katerih vsota preseže limit int-a.
```php
function vsota(int $a, int $b) : int|float {
	return $a + $b;
}
```
