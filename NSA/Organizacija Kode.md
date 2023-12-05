1. Potiskanje funkcionalno zaključenih delov kode na konec datotek. 
2. Izločevanje funkcionalno zaključenih blokov kode v drugo datoteko, kot `#include`
	- V PHP se uporablja `include` ali `include_once`, če želimo da preverja za ponovne definicije funkcij.
	- Če je datoteka nujno potrebna, in hočemo da vrže error (in s tem ustavi program), ne le, da izpiše warning, uporabljamo `require` in `require_once`.