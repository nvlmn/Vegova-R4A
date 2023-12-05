Right outer join
```sql
--Desna tabela (oseba) je “glavna”, ker iz nje vedno izpišemo vse
SELECT * FROM KRAJ K RIGHT OUTER JOIN OSEBA O ON K.POSTA=O.POSTA;
```

Left outer join, ki doseže enako:
```sql
SELECT * FROM OSEBA O RIGHT OUTER JOIN KRAJ K ON O.POSTA=K.POSTA;
```

Full outer join (ne mešat z unijo):
```sql
SELECT * FROM KRAJ K FULL OUTER JOIN OSEBA O ON K.POSTA=O.POSTA;
```
To izpiše vse vrstice iz leve, vse iz desne, in tiste, ki so vsebovane v obeh. 

Natural join (avtomatično popaira atribute z enakim imenom):
```sql
SELECT * FROM KRAJ K FULL NATURAL JOIN OSEBA O;
```