# Tabla horizontal

Dado el siguiente HTML:

```html
<!doctype html>
<html>
	<html>
		<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

		<script>
			//aquí código JavaScript
		</script>
	</html>
	<body>
		<div>
			<div>
				<button data-show-books>Mostrar libros</button>
				<button data-show-publishers>Mostrar editoriales</button>
			</div>
			<div data-content></div>
		</div>
	</body>
</html>
```
Se quiere que al hacer click en el botón `Mostrar libros` se muestre un listado de libros, lo mismo para editoriales.

Los libros se pueden obtener con una llamada REST, `GET /books`; lo mismo para editoriales, `GET /publishers`.

> Nota: Crear dos funciones (una para libros y otras para
> editoriales) que devuelvan una promesa con el JSON de ejemplo, así se
> evitan llamadas reales a un servidor.

Un ejemplo de lo que devuelve libros es el siguiente:

```javascript
{
    data: [
        {
            id: 1,
            name: 'El nombre del viento',
            pages: 300,
            publisher: 'Santillana'
        },
        {
            id: 2,
            name: 'La caida de los gigantes',
            pages: 540,
            publisher: 'SM'
        },
        {
            id: 3,
            name: 'El nombre de la rosa',
            pages: 267,
            publisher: 'SM'
        }
    ]
}
```

Un ejemplo de lo que devuelve la llamada a editoriales es el siguiente:

```javascript
{
    data: [
        {
            id: 1,
            name: 'Santillana',
            books: 1
        },
        {
            id: 2,
            name: 'SM',
            books: 2
        }
    ]
}
```

Se quiere un archivo JavaScript que, utilizando jQuery, al pulsar en los botones correspondientes muestre en una tabla el contenido del servidor (en el elemento `data-content`).

La tabla para los libros debe mostrarse horizontal, de la siguiente manera (obviar primera fila, aparece así por temas de markdown):

&nbsp;         | &nbsp;                   | &nbsp; | &nbsp;
------         | -----                    | -----  | -----
**Nombre**     | El nombre del viento     | 300    | Santillana
**Páginas**    | La caida de los gigantes | 540    | SM
**Editorial**  | El nombre de la rosa     | 267    | SM

Lo mismo para las editoriales:

&nbsp;     | &nbsp;     | &nbsp;
------     | -----      | -----
**Nombre** | Santillana | 1
**Libros** | SM         | 2
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM3NDU0Njc4MiwtNDg4MzgyNTA2LDExMT
UyMjc4MTBdfQ==
-->