```html
<form>
	a <input type=“text” name=“a” value=“0” />
	b <input type=“text” name=“b” value=“0” />
	<input type=“submit” />
</form>
```

```php
<?php
	/* vsota.php */
	/* koda, ki checka tipe, $_GET vrednosti prestavi v local variable, ..._*/
	$vsota = $_GET[’a’] + $_GET[’b’];
	echo $vsota;
	echo ‘<a href=“index.php”>Klikni za nazaj</a>’;
?>
```

#### 28. 11. 2023
```php
/* Forma za:
	- izbiro spola (obvezno samo en) 
		  in
	- izbiro maturitetnega predmeta.
*/
echo ‘
<form>
<input type=“radio” name=“spol” value=“musko” /> Muško
<input type=“radio” name=“spol” value=“zensko” /> Žensko
<input type=“radio” name=“spol” value=“stajeovo” checked=“checked” /> Pa šta je ovo muško il žensko
<input type=“submit” name=“1”/>
</form>
‘;

echo ‘
<form>
<input type=“checkbox” name=“predmet[]” value=“mat” /> MAT
<input type=“checkbox” name=“predmet[]” value=“ang” /> ANG
<input type=“checkbox” name=“predmet[]” value=“fiz” /> FIZ
<input type=“checkbox” name=“predmet[]” value=“psi” /> PSI
<input type=“checkbox” name=“predmet[]” value=“seminarska” /> SEMINARSKA
<input type=“submit” name=“2”/>
</form>

if (isset($_GET[”predmet”]])) 
	foreach ($_GET[”predmet”] as $k => $v)
		switch ($v) {
			case “mat”:
				echo ‘<p>MAT</p>’;
				break;
			case “ang”:
				echo ‘<p>ANG</p>’;
				break;
			case “fiz”:
				echo ‘<p>FIZ</p>’;
				break;
			case “psi”:
				echo ‘<p>PSI</p>’;
				break;
			case “seminarska”:
				echo ‘<p>SEMINARSKA</p>’;
				break;
			default:
				break;
		}
‘;
```

