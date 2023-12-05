- naključna generacija: slabo razlikovanje
- pseudorealni (iz “dictionarya”)
	- format/oblika (zaporedje imena in priimka, valute …)

Sestavimo par slovarjev, generiramo podatke:
```php
function randIme() 
{
	$imena = [‘Mihec’,‘Tobi’,‘Amin’];
	
	return $imena[rand(0,count($imena)-1)];
}

function randPriimek() 
{
	$priimki = [...];
	
	return $priimki[rand(0,count($priimki)-1)];
}

echo randIme();
echo randIme();
echo randIme();
echo randIme();

echo randPriimek();
echo randPriimek();
echo randPriimek();
echo randPriimek();

function randOseba() 
{
	return randIme() . ”” . randPriimek();
}

$osebe = Array();

for ($i = 0; $i < 30; $i++)
	$osebe[] = randOseba();
```

Koda, na kateri delamo, na: https://gitlab.vegova.si/serhio.w02/ropotarnica


