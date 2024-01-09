# Apuntes Bootstrap

## Como añadir Bootstrap a un proyecto

Simplemente con añadir las siguientes líneas al \<head\> de nuestro proyecto será suficiente:

```html
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL"
        crossorigin="anonymous"></script>

```

Esto hará que el desde el cliente al ejecutar nuestra web se descarguen automáticamente las dependencias de Bootstrap, para la versión ahí especificada, en este caso es la 5.2.2.

## Los tres pilares de Bootstrap

### El Grid

Nos va a permitir estructurar los elementos de la web y como van a adaptarse los elementos de la web.

El Grid es una cuadrícula imaginaria que nos va a permitir definir cómo queremos que se presenten los elementos de la web y qué espacio van a ocupar. La grid de Bootstrap es un conjunto de contenedores, filas y columnas que definen cómo se va a presentar y alinear el contenido.

La cuadrícula nos va a permitir trabajar por filas y columnas, pero cada fila está dividida en 12 columnas. Esto quiere decir que podemos indicar cuántas columnas queremos que ocupe cada elemento en una fila, hasta un máximo de 12 (entre todos los elementos de la fila).

#### Clases para la Grid

* .row : Al agregar la clase row estamos diciendo que el elemento que contenga esta clase será tratado como una fila. 
* .col- : La clase col nos dice cuántas columnas va a ocupar en la fila este elemento (entre 0 y 12). Tamaño de columna extra pequeña, por defento.
* .col-xs- : Tamaño de columna extra pequeña
* .col-sm- : Tamañod e columna pequeña
* .col-md- : Tamaño de columna mediana
* .col-ls- : Tamaño de columna grande
* .col-xl- : Tamaño de columna extra grande
* .col-xxl- : Tamaño de columna extra extra grande

![Imagen relaciçión tamaños pantalla](res/col-sizes.png)

#### Breakpoints en Bootstrap

Dimensión (ancho) a partir de la cuál podemos cambiar el estilo o la estructura de la web. Esto se refiere a los tamaños de pantalla en los que cambiamos de "tipo" de pantalla para aplicar un cambio de tamaño u ocultar o mostrar algún elemento y ayudar a la responsividad del sitio.

#### Estructura de la Grid

Un contenedor (container), como ya adelantábamos, puede contener filas y cada fila contiene 12 columnas. 

Una estructura simple podría ser algo así:

```html
<div class="container">
    <div class="row">
        <div class = "col"></div>
        <div class = "col"></div>
    </div>
    <div class="row">
        <div class = "col"></div>
        <div class = "col"></div>
        <div class = "col"></div>
    </div>
</div>
```

Un container en bootstrap es un elemento html que va a contener toda la estructura de filas y columnas, tenemos dos clases específicas para crear estos contenedores:

* .container : Esta clase crea un contenedor responsivo con un ancho máximo fijo que depende del tamaño del dispositivo
* .coontainer-fluid : Esta clase crea un contenedor respnosivo que cubre el 100% del ancho de la ventana. 

```html
    <div class="container">
        .container
    </div>
    <div class="container-fluid">
        .container-fluid
    </div>
```

En Bootstrap, se pueden asignar los siguientes tamaños a un container:

* .container-sm: Tamaño pequeño.
* .container-md: Tamaño mediano.
* .container-lg: Tamaño grande.
* .container-xl: Tamaño extra grande.
* .container-xxl: Tamaño extra extra grande.

Estas clases se pueden utilizar para crear contenedores responsivos con diferentes anchos máximos dependiendo del tamaño del dispositivo.

En los anchos de pantalla en los que pueden expandirse, los contenedores van a comportarse como un container-fluid, en el momento en el que llegan a su breakpoint, vuelven a comportarse como un container normal.

##### Filas y columnas

Los elementos html pueden ocupar una o varias columnas, siempre dentro de las 12 máximas de la fila, pero repartiendo dichas columnas como queremos repartir el ancho de la misma. 

Las columnas de los elementos de una fila siempre deben sumar 12 para que estén ubicadas en una misma línea, si sumamos más de las 12, el excedente se irá a una nueva línea.

La cantidad de filas y columnas que pueden ocupar puede que no queramos que sea la misma en todos los tamaños de pantalla, para ello, podemos asignar diferentes cantidades dentro de las posibles 12 columnas según el tamaño, en el ejemplo siguiente vemos dos elementos que ocupan 4 y 8 columnas para tamaños pequeños y 6 y 6 para tamaños grandes respectivamente:

```html
        <div class="row">
            <div class = "col-sm-4 col-lg-6">
                .col-sm-4 .col-lg-6
            </div>
            <div class = "col-sm-8 col-lg-6">
                .col-sm-8 -col-lg-6
            </div>
        </div>
```


### Los Componentes

Elementos HTML reutilizables con un estilo ya predeterminado. Además, también podremos personalizar ese estilo ya predeterminado completamente a nuestro gusto.





### Los iconos

Iconos gratuitos que podemos utilizar en nuestras webs, por ejemplo, iconos de las RRSS más utilizadas. 

