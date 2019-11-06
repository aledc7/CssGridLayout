## Ejemplo de una pagina con un Header, un Footer, y 2 divs centrales


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
            grid-template: 1fr 7fr 1fr / 1fr 1fr;
            grid-gap: 5px;
            height: 100vh;

            /* esta propiedad es para especificar areas, va separado por comillas dobles */
            grid-template-areas: "header header "
                                 "left right " 
                                 "footer footer ";
        }
        .item{
            background: lightblue;
            padding: 10px;
            border: 1px solid red;
        }
        .header{
            /* propiedad aplicada a los grid items */
         grid-area: header;
         background: lightslategray;
         color: white;
         text-align: center;
         font-size: 40px;
        }
        .left{
            grid-area: left;
            text-align: left;
            font-size: 20px;
            color: blue;
        }
        .right{
            grid-area: right;
            text-align: center;
            font-size: 40px;
        }
        .contenido{
            grid-area: contenido;
            text-align: center;
            font-size: 40px;
        }
        .footer{
            grid-area: footer;
            background: lightslategrey;
            color: white;
            text-align: center;
            font-size: 40px;
        }

    </style>
</head>
<body>
    <section class="container">
        <div class="item header ">Cabecera</div>
        <div class="item left ">Presupuesto Original
            <ul>
                <li>Item de Presupuesto</li>
                <li>Item de Presupuesto</li>
                <li>Item de Presupuesto</li>
                <li>Item de Presupuesto</li>
                <li>Item de Presupuesto</li>
                <li>Item de Presupuesto</li>
            </ul>  
        </div>
        <div class="item right ">Presupuesto Nuevo</div>
        <!-- <div class="item contenido ">contenido</div> -->
        <div class="item footer">Pie de Página</div>
    </section>
    
</body>
</html>

````

