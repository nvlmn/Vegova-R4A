```sql
ALTER TABLE ime_tabele ADD/DROP atribut;
```

### Dodajanje omejitve (check constraint)
```sql
ALTER TABLE oseba ADD CONSTRAINT id_osebe PRIMARY KEY(emso);
```

**Ne-standardno (ALT. TABLE + ALT.COLUMN) !! :**
```sql
ALTER TABLE oseba ALTER COLUMN primek TO priimek;
ALTER TABLE oseba ALTER COLUMN priimek TYPE CHAR(50);
ALTER TABLE oseba ALTER COLUMN emso POSITION 1;
```

==**V SQL se večina stvari (npr. position) štejejo od 1, ne od 0. **==

Napišite SQL stavek, ki bo atribut cena (v tabeli CD) spremenil tako, da bo ta tipa float (zdaj je int) ter spremeni pozicijo atributa tako, da bo zdaj 2. zapor., za ID-jem.
```sql
ALTER TABLE cd ALTER COLUMN cena POSITION 2;
ALTER TABLE cd ALTER COLUMN cena TYPE FLOAT;
```
