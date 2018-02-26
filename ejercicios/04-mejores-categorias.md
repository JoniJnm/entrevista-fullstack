# Mejores categorías

Dada la siguiente estructura en MySQL:

```sql
CREATE TABLE `CATEGORIES` (
  `ID_CATEGORY` int(11) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  `NAME` varchar(255) NOT NULL,
  `ID_CATEGORY_PARENT` int(11) NOT NULL,
  `POSTS` int(11) NOT NULL DEFAULT '0'
);
```

Crea una sentencia `select` que devuelva las categorías de cada nivel (`ID_CATEGORY_PARENT`) con más número de POSTS. Si es necesario, crea índices para aumentar su rendimiento.

Por ejemplo, para el siguiente listado:

ID_CATEGORY  | NAME  | ID_CATEGORY_PARENT  | POSTS
------ | ------ | ------ | ------ | 
1 | root | 0 | 0
2 | Películas | 1 | 25
3 | Ciencia ficción | 2 | 5
4 | Horror | 2 | 15
5 | Libros | 1 | 4
6 | Fantasía | 5 | 7
7 | Romance | 5 | 7
8 | Autoayuda | 5 | 7

Debe devolver:

ID_CATEGORY  | NAME  | ID_CATEGORY_PARENT  | POSTS
------ | ------ | ------ | ------ | 
1 | root | 0 | 0
2 | Películas | 1 | 25
4 | Horror | 2 | 15
6 | Fantasía | 5 | 7
7 | Romance | 5 | 7
8 | Autoayuda | 5 | 7

Crea otra sentencia que devuelva las dos categorías con mayor número de posts por nivel. En el ejemplo anterior, el nivel de Libros (`ID_CATEGORY_PARENT  =5`) tiene 3 resultados, deberían devolverse sólo dos de ellos (a escoger).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgxOTQyNTM5M119
-->