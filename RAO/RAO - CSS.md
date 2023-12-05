### Načini uporabe
- Ločena datoteka .css
	<link rel=“stylesheet” type=“text/css” href=“styles.css”>
	
	styles.css:
```css
p {
	color: blue;
}

h1 { 
	color: red;
}
 ```
- Znotraj HTML (\<style> tag)
- Znotraj značke (kot atribut, npr. <p style=“color: blue;”>lalalala</p>) — **ne uporabljaj, ker ti bo Podpadec automatično dau 1, mby kemično kastriru**

## Načini selekcije
#### ID
Vsak element ima lahko samo 1 ID.
Vsaka stran ima lahko samo 1 element s tem ID.
```css
#mojID {
	color: blue;
}
```
#### Class
```css
.mojClass {
	color: blue;
}
```
#### Tag
```css
p {
	color: blue;
}

h1 { 
	color: red;
}
 ```

### CSS box model
![[Pasted image 20230914122724.png]]

```js
let tabela = document.createElement(“table”);
document.body.appendChild(tabela);

for (let i = 0; i < 8; i++) {
	let vrtsica = document.createElement(“tr”);
	tabela.appendChild(vrstica);
	
	for (let j = 0; j < 8; j++) {
		let celica = document.createElement(“td”);
		vrstica.appendChild(celica);
	
		if ((i+j)%2 === 0) celica.style.backgroundcolor=“black”;
		else celica.style.backgroundcolor=“gray”;

		celica.onClick = kilk;
		// Isto z Listenerjem:
		celica.addEventListener("click", function() => {
			if (this.className === “bela”) this.className = “crna”;
			else this.className = “bela”;
		});
	}

	tabela.appendChild(vrstica);
}

function klik {
	if (this.className === “bela”) this.className = “crna”;
	else this.className = “bela”;
};
```

### Šahovnica brez tabele (npr. z div)
```html
<html>
	<head>
		<style>
			.body {
				display: grid;
				grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
				width: 400px;
			}
			
			.crna {
				background-color: black;
				height: 50px;
				width: 50px;
			}
			
			.bela {
				background-color: lightgray;
				height: 50px;
				width: 50px;
			}
		</style>
	</head>
	<body>
		<script>
			for (let i = 0; i < 8; i++)
				for (let j = 0; j < 8; j++) {
					let polje = document.createElement(“div”);
					polje.className = ((i+j)%2)?”crna”:”bela”;
					
					polje.addEventListener(“click”,function(){
						console.log(this);
					}
					
					// S puščično funkcijo:
					polje.addEventListener(“click”, () => {
						console.log(polje);
					}		
				);
					
					document.body.appendChild(polje);
				}
		</script>
	</body>
</html>
```

[[CSS Pseudo-Classes]]