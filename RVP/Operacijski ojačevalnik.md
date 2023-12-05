![](https://www.circuitstoday.com/wp-content/uploads/2011/11/inverting-amplifier-using-opamp.png)

1. a = $\inf{}$
2. A = $\frac{U_izhod}{U_uhod}$
3. $U_0 = 0\ V$

![[Pasted image 20230928125435.png]]

Siemens PLC ima 10-bit ADC, enako kot Arduino oz. Atmle Atmega328p. 

Pri Siemensu se upošteva leva poravnava v registrih:
- prvi bit ($b15$) je rezerviran za predznak,
- 10 bitov je podarkov,
- 5 jih je neuporabljenih.

## Primerjalnik napetosti
$V_- = 1\ V$
$V_+= 9\ V$
##### Tokovi
$I_{D1} = I_{D2} = 0\ mA$
$I_1 = I_2 = 1\ mA$

##### Vhodne napetosti
$V_- = I_1*R_3 = 1 V$
$V_+ = I_2*R_4 = 9 V$

##### Diferenčna napetost
$U_D = |V_+-V_-| = 8 V$

$U_{IZH} = 20\ V$





### Sprašuje
- o bitnosti AD pretvornikov (npr. prvi bit je predznak),
- operacijski ojačevalnik 
	- kaj smo predpostavili?
		- A = $\infty$
		- $U_D = 0\ V$ (pri negativni povratni vezavi)
		- $R_D = \infty$
	- primerjalnik napetosti,
- leva/desna poravnava. 