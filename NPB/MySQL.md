CLI orodje (SQL konzola): `mysql -u root -p`.

Domen ni. Kvazi nadomestek je ENUM. 

Pomembni tipi:
- INT
- FLOAT
- CHAR/VARCHAR
- TIMESTAMP
- ENUM (nadomestek domen)

MyISAM je prejšnji backend MySQL-a. Zdaj je InnoDB.
Podpore za ACID v MyISAM ni bilo, ne podpira FK (le PFK).
Ni podpiral arhiviranja, restavriranja. 
InnoDB omogoča zaklepanje posameznih vrstic, MyISAM le tabel. 

Po `CREATE TABLE (podatki …)`, ali `CREATE DATABASE` lahko dodamo: 
	`ENGINE = innoDB / MyISAM`
	`auto_increment=100` — korak je vedno 1, 100 je prva št. ki jo auto increment dodeli
	`character set utf8`

Pred vnosom vrednosti v ENUM tip nastavimo:
```sql
SET @@GLOBAL.SQL_MODE=‘strict_all_tables’;
```

#### Razlika pri alter
```sql
-- Atributa “AFTER” v SQL standardu ni, MySQL ga podpira:
ALTER TABLE HOTELI ADD OPIS CHAR(20) AFTER IMEHOTELA; 
-- Na prvo mesto:
ALTER TABLE HOTELI ADD ID INT NOT NULL FIRST; 
ALTER TABLE KRAJI DROP OPISKRAJA;
```

#### Drop
```sql
DROP TABELA; -- Droppa tabelo. Faila, če je PK (starševska tabela)
```

#### Alter table + MODIFY/CHANGE
```sql
ALTER TABLE HOTELI MODIFY OPIS CHAR(8) NOT NULL;
--PREIMENUJE OPIS -> OPISHOTELA
ALTER TABLE HOTELI CHANGE OPIS OPISHOTELA CHAR(8) NOT NULL;
```

**==Modify==** lahko spremeni: 
- tip
- omejitev
- lega
**==Change==** pa poleg vsega tega še:
- ime

##### Primer
```sql
--POSITION 1 NE BI DELAL V MySQL:
ALTER TABLE HOTELI MODIFY `ImeHotela` VARCHAR(50) NOT NULL FIRST;
```

#### Spreminjanje constraintov
```sql
--ENAKO KOT V FIREBIRD:
ALTER TABLE HOTELI ADD CONSTRAINT … ; 
```

```sql
--ENAKO KOT V FIREBIRD:
ALTER TABLE OSEBA DROP CONSTRAINT PRIMARY KEY; 
ALTER TABLE OSEBA ADD CONSTRAINT nov_pk PRIMARY KEY(emso, davcna);
```

### Pregled sheme v MySQL
```sql
--POLNA SHEMA:
SHOW CREATE TABLE TBELA;
--SIMPLIFIED SHEMA
DESCRIBE IME;
```