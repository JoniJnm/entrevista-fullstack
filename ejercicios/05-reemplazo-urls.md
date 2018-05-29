# Reemplazo URLs

Se quiere una función llamada `convertLinks` al que se le pasa un contenido HTML y reemplaza los enlaces de los elementos `<a>` por una URL propia donde se hará la redirección.  La URL de reemplazo es `https://go.com` al que se le pasa un argumento `url` donde irá  la URL original.

Crea la función en PHP y en JavaScript.

A tener en cuenta:

 - Sólo se reemplazarán enlaces cuyo protocolo sea `http` o `https`
 - El contenido HTML vendrá bien formado (puede haber atributos envueltos en comillas dobles `"` o simples `'`)

Para el siguiente ejemplo:

```html
<div id="footer">
	<p><a href="/" 
		data-href="https://github.com">Página principal</a>
	</p>
	<p><a class="prueba" href="https://github.com">Github</a></p>
	<p><a href='https://www.google.es/search?q="volar rápido"'>Volar rápido</a></p>
</div>
```

Debería devolver:

```html
<div id="footer">
	<p><a href="/" 
		data-href="https://github.com">Página principal</a>
	</p>
	<p><a class="prueba" href="https://go.com/?url=https%3A%2F%2Fgithub.com">Github</a></p>
	<p><a href='https://go.com/?url=https%3A%2F%2Fwww.google.es%2Fsearch%3Fq%3D%22volar+r%C3%A1pido%22'>Volar rápido</a></p>
</div>
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA3NjA3NTE3NywyMDgxNTEzMzExXX0=
-->