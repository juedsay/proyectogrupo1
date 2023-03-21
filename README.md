# Proyecto Grupo

> En general, en los repositorios GIT no se suben binarios or imagenes, pero en este caso lo hago solamente para incluirte un screenshot the como se ve lo que me manaste.

Lo que tenes que corregir es que estas usando posiciones absolutas.

Cuando usas bootstrap, y sobre todo las grillas, te tenes que imaginas que:

1 grilla siempre mide 12 unidades de ancho.

Si queres tener un side bar, en resolution grande, podrias dividir la grilla end 2:

1. La primera que va a ser un col-10 (aqui colocas el listado de articulos)
2. La segunda que es la side bar un col-2 (aqui colocas el side-bar)

Luego dentro de la primera, colocas de nuevo otra grilla en la que cada uno de los articulos va a ocupar 4 unidades (porque lo queres dividir en 3 columns, y la grilla tiene 12 unidades, entonces 12 dividido en 3 columnas, 4 unidades por columna)

Ahora, esto es considerando que para todas las resoluciones va a ocupar lo mismo.

si vos queres hacer que para la resolucion de pantallas pequeñas, medianas y grandes tenga diferentes formatos, ahi entran las unidades de medida: col-md-X, col-sm-X

por ejemplo si queres que en mobile haya una sola columna tu formato deberia ser algo asi como:

1. La primera que va a ser un col-10 col-sm-12 (aqui colocas el listado de articulos)
2. La segunda que es la side bar un col-2 col-sm-12 (aqui colocas el side-bar)

Aqui podes ver que especifico para pantalla pequeña (con -sm-) que ocupe las 12 unidades, y que el default sea col-10 o col-2 dependiendo del elemento.

Ahora lo siguiente que hay que ver es el contenedor donde definis estas columnas:

"container-fluid" va a ocupar el 100%. Por lo tanto tendrias que hacer el main, y el contenedor de las dos columnas un fluid, y agregarle la clase "row" para colocar todas las columnas una al lado de otra

Otra idea podría ser directamente utilizar sidebars de Bootsrap
https://getbootstrap.com/docs/5.0/examples/sidebars/

Y Aqui tenes documentación de las grillas:
https://getbootstrap.com/docs/4.0/layout/grid/
