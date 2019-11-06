![Css](https://raw.githubusercontent.com/aledc7/CssGridLayout/master/resources/cssGridLayout.png)


[![aledc.tk](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/aledc.com.svg)](https://aledc.tk)
[![ingenea.com.ar](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/ingenea.svg)](http://ingenea.com.ar)
[![License](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/mit-license.svg)](https://aledc.com)
[![GitHub release](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/release.svg)](https://aledc.com)
[![Dependencies](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/dependencias-none.svg)](https://aledc.com)


# Css Grid Layout


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        body{
            font-family: Arial;
        }
        .container{
            /* Esta propiedad "grid" es la que hace toda la magia */
            display: grid;

            /* Puedo indicar el tamaño de filas y columnas en lineas por separado */

            /* grid-template-columns: 10% 200px 40%; */
            /* grid-template-rows: 300px 300px; */

             /* O puedo hacerlo con el "modo abreviado" 
                                 filas      /   columbas */
            /* grid-template: 300px 50px 100px / 10% 200px 40%; */

            /* Otra manera de distribuir la pantalla es utilizando la unidad fr (de fraccion)
            en este caso al utilizar 3 veces 1 fr,  se dividirá en 3 partes iguales */

            grid-template: 300px 50px 100px / 1fr 1fr 1fr;

            /* FUNCIONES */

            /* Grid Layout ahora soporta el uso funciones, por lo que si quisiera repetir lo mismo 
            de arriba sin tener que escribir x veces 1fr podría hacerlo mediante una funcion: */

            /* Funcion repeat(cantidad, elemento) */

            /* grid-template: 300px 50px 100px / repeat(4, 1fr); */


            /* Funcion minmax() 
                Esta funcion permite extablecer el tamaño minimo y maximo que tendrá un elemento de la grilla.
            */

            grid-template: 300px 50px 100px / repeat(4, minmax(100px,1fr));


            /* Agregar espacios entre filas y columnas en una linea para fila y otra para columna */
            /* grid-column-gap: 30px;
            grid-row-gap: 10px; */

            /* Agregar espacion entre filas y columnas de manera abreviada en una sola linea */
            /*        fila / columna    */
            grid-gap: 10px   30px;
        }
        .item{
            background: lightblue;
            padding: 10px;
            border: 1px solid red;
        }
        .item:nth-of-type(4){
            background: lightgreen;

            /* con esta propiedad  overflow hago que se pueda escrolear */
            overflow:auto;
        }
        .item .item{
            color: white;
            padding: 5px;
            background: blue;
            grid-column-gap: 5px;
            grid-row-gap: 10px;
        }

    </style>
</head>
<body>
    <section class="container">
        <div class="item">contenido #1</div>
        <div class="item">contenido #2</div>
        <div class="item">contenido #3</div>
        <div class="item">
            <div class="item">subitem #1</div>
            <div class="item">subitem #2</div>
            <div class="item">subitem #3</div>
            <div class="item">subitem #4</div>
            <div class="item">subitem #5</div>
            <div class="item">subitem #6</div>
            <div class="item">subitem #7</div>
            <div class="item">subitem #8</div>
            <div class="item">subitem #9</div>
            <div class="item">subitem #10</div>
        </div>
        <div class="item">contenido #5</div>
        <div class="item">contenido #6</div>
        <div class="item">contenido #7</div>
        <div class="item">contenido #8</div>
        <div class="item">contenido #9</div>
        <div class="item">contenido #10</div>
        <div class="item">contenido #11</div>
        <div class="item">contenido #12</div>

    </section>
    
</body>
</html>
```

