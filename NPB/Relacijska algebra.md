Gre za podvrsto matematike, na kateri temleji DQL stavek. 

#### Osnovne operacije
- Selekcijo
- Razliko
- Kartezični produkt
- Projekcijo
- Unijo

#### Izvedene operacije
Te lahko zapišemo kot kombinacijo osnovnih. 
- Presek
- Naravni stik
- Theta stik
- Količnik

### Selekcija
Ko uporabimo ==WHERE==.

### Projekcija
Ko uporabimo \*, seznam atributov … 
==Izberemo stolpce za prikaz==

### Kartezični produkt
Je nezaželena operacija. Največkrat jo nardiš po nesreči. 

### Unija
Unija je implementirana s pomočjo standardne rezervirane besede UNION znotraj stavka SELECT. 

Union lahko delamo nad tabelami/SELECT stavki, ki imajo enak tip, število, in zaporedje stolpcev. 

### Razlika

### Theta stik
Je filtriran kartezični produkt.
Oblika `SELECT * FROM TABELA1 T1, TABELA2 T2 WHERE T1.SK_ATRIBUT=T2.SK_ATRIBUT`.

### Naravni stik
Implementiran je z rezervirano besedo join. 
Pred združitvijo (stikom) preveri enakost celic, po katerih jih stika, ne le po stiku, kot theta. 

Implementiran je z `JOIN` stavki. 
