# Mostrar objeto

Crea una función llamada `dump` que dado un objeto devuelva un `string` en que el cada línea muestra la claves y valores del objeto. 

 - Admitido: JavaScript
 - El objeto de entrada sólo contendrá números, cadenas de texto, arrays u objetos

Para el siguiente objeto:

```javascript
{
	nombre: "Pedro",
	edad: 45,
	direccion: {
		localidad: "Parla",
		provicia: "Madrid"
	},
	estudios: [],
	hijos: [
		{
			nombre: "Juan",
			edad: 13
		},
		{
			nombre: "María",
			edad: 15
		}
	]
}
```

Debe devolver:

```
nombre: "Pedro"
edad: 45
direccion: Object
direccion.localidad: "Parla"
direccion.provicia: "Madrid"
estudios: Array
descripcion: "Soy un apasaionado del cine.\nMe gustan películas como \"A todo gas\" o \"Los vengadores\"."
hijos: Array
hijos[0]: Object
hijos[0].nombre: "Juan"
hijos[0].edad: 13
hijos[1]: Object
hijos[1].nombre: "María"
hijos[1].edad: 15
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0NDI4NzczMDFdfQ==
-->