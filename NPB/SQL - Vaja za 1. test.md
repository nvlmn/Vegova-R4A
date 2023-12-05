File z vprašanji na Moodle: https://moodle2.vegova.si/pluginfile.php/70806/mod_folder/content/0/NPB_tutorial1.docx?forcedownload=1



g) Imena oddelkov iz Ljubljane, ki imajo več kot 10 zaposlenih računalniških tehnikov (rač. tehnik je poklic).
```sql
SELECT O.ImeOddelka 
FROM ODDELEK O 
INNER JOIN DELAVEC D ON 
	(O.ODDELEKID = D.ODDELEKID)
WHERE D.KRAJ = ‘Ljubljana’ AND D.POKLIC = ‘Računalniški Tehnik’
GROUP BY O.ImeOddelka
HAVING COUNT(*) >= 10;
```

m) 
```sql
SELECT O.ImeOddelka 
FROM ODDELEK O 
LEFT JOIN DELAVEC D ON 
	(O.ODDELEKID = D.ODDELEKID)
WHERE D.POKLIC = ‘Računalniški Tehnik’
GROUP BY O.IMEODDELKA
HAVING COUNT(D.DELAVECID) = 0;
```

l) 
```sql
SELECT ImeOddelka
FROM Oddelek
LEFT OUTER JOIN DELAVEC D ON
	(O.ODDELEKID = D.ODDELEKID)
WHERE O.KRAJ = D.KRAJ
GROUP BY ODDELEK
HAVING COUNT(*) >= 3;
```
