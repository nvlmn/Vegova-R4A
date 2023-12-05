Dodajanje, brisanje in spreminjanje podatkov.

Vse kar te stavki delajo: insert, update, delete, se imenuje transakcija. Ena transakcija lahko spremeni več zapisov. 

#### ACID
- Atomarnost (atomicity): ==Vsaka transakcija se mora izvršiti v celoti, ali pa se sploh ne.==
- Celovitost (consistency): ==Ne sme priti do slučaja, kjer so v bazi orphan zapisi: to je ta feature, ki ne pusti brisanja srarševskih tabel.==
- Izolacija (isolation): ==Transakcija se časovno omeji (beleži se kdaj je prišla v SUPB), da se dve ne izvajata na enkrat.==
- Trajnost (durability)

### Insert
```sql
INSERT INTO ime_tabele VALUES (v1, v2, v3, …);
--ALI:
INSERT INTO ime_tabele (polje1, polje2) VALUES (v1, v2);
--V MySQL lahko vstavimo več vrstic naenkrak, a ni standardno:
INSERT INTO ime_tabele VALUES ROW(v1a, v2a), ROW(v1b, v2b), ROW(v1c, v2c);
--ALI:
INSERT INTO ime_tabele (polje1, polje2, polje3) VALUES ROW(v1a, v2a, v3a), ROW(v1b, v2b, v3b), ROW(v1c, v2c, v3c);
```

### Update
```sql
UPDATE ime_tabele SET ime_atributa = nova_vrednost, …;
--ALI
UPDATE ime_tabele SET ime_atributa = nova_vrednost, … WHERE pogoj;
--Primer
UPDATE Dijak D SET D.Priimek = UPPER(D.Priimek), D.Razred=UPPER(D.Razred);
UPDATE Dijak D SET Tocke = CAST(SUBSTRING(Razred from 2 for 1) AS INTEGER) + 10;
UPDATE Dijak D SET Vzdevek = NULL WHERE (PRIIMEK LIKE ‘B%’);
UPDATE Dijak D SET Vzdevek = NULL WHERE (Priimek <> Upper(Priimek));
```
