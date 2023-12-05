Z njimi definiramo svoje podatkovne tipe, ki bazirajo na že obstoječih. 

#### Primeri
```sql
CREATE DOMAIN Ocena INTEGER DEFAULT 1 NOT NULL CHECK (VALUE BETWEEN 1 AND 5);

CREATE DOMAIN TelefonskaST CHAR(12) CHECK (VALUE LIKE ‘+386%’);
```

#### Vaja 
1. Napišite SQL stavek, ki ustvari domeno DDV, ki je tipa float, obvezen za vnos (NN), privzeta vrednost naj bo 22. V check stavku zagotovimo, da je vrednost te domene lahko enaka le 9.5 ali 22.
```sql
CREATE DOMAIN DDV FLOAT DEFAULT 22 NOT NULL CHECK (VALUE IN (9.5, 22));
```
