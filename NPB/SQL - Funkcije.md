### Uvod
#### Tri vrste
1. Vgrajene (agregirane) funkcije
	- SUM
	- AVG
	- MIN
	- MAX
	- COUNT
2. Standardne (niso del standarda, ampak jih imajo “načeloma” vsi SUPB-ji v stavku `SELECT`)
	- UPPER
	- LOWER
	- SUBSTRING
	- EXTRACT
	- CAST
1. Nestandardne (UDF)
	- YEAR
	- MONTH
	- RANDOM
	- FLOOR

Samostojna agregirana funkcija se izvede nad vsemi vrsticami tabele.
```sql
SELECT FUNKCIJA(attrx) FROM tabela;
```
Z združevanjem: 
- Pred izvedbo agregirane funkcije se vrstice tabele združijo glede na pogoj.
- Agregirana funkcija se za vsako skupino vrstic **izvede posebej**.
```sql
SELECT FUNKCIJA(attrx), attry, attrz FROM tabela GROUP BY attry; --ali attrz
```

==Agregirane funkcije ignorirajo vrednost **NULL**.==

### Vaja “srednje težke” poizvedbe
Napišite poizvedbo, ki bo vrnila imena kategorij in imena izdelkov ter povprečno ceno izdelkov, za vse tiste izdelke, ki jih dobavljajo dobavitelji “petrol”, “mol”, za katere velja da je njihova povp. dobavna cena pod 1 eur.

```sql
SELECT K.IMEKATEGORIJE, I.IMEKATEGORIJE, AVG(CENA) AS ‘POVPRECNA CENA’
FROM KATEGORIJA K 

INNER JOIN IZDELEK I ON (K.KID = I.KID) 
LEFT JOIN DOBAVLJA D ON (D.ID = I.ID)
INNER JOIN DOBAVITELJ DD ON (DD.DID = D.DID)

WHERE IMEDOBAVITELJA IN (’petrol’, ‘mol’, ‘agip’)
HAVING AVG(CENA) < 1;
```