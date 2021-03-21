# CURSO DE DISEÑO WEB CON CSS GRID Y CON FLEXBOX

## DESCUBRE QUE HA CAMBIADO EN NUESTRO MEDIO

### TODO SOBRE EL DISEÑO DE PAGINAS WEB HA CAMBIADO

- El diseño gráfico en la web ha evolucionado significativamente dúrate los últimos 25 años
	- Inicialmente se tenía una paleta de 216 colores
	- Las tipografías eran limitadas
- Con la llegada y avance de CSS ha mejorado la web
	- CSS Grid ⇒ nueva tecnología poderosa para crear layouts

**Consejos de @teffcode**

- Probar y jugar las nuevas características de CSS
- No construir los mismos diseños antiguos con las mismas tecnologías antiguas
- Descubre todo lo que ha cambiado
- No asumas que ya sabemos en qué se convertirá la web. O que ya lo hemos dominado todo.
- No existe una forma “correcta” de hacer los diseños

------------


[========]

## CONCEPTOS QUE FORMAN PARTE DEL DISEÑO CSS

### IMPORTANCIA DE RECORDAR LAS HERRAMIENTAS EXISTENTES
- [Curso Recomendado](https://platzi.com/clases/css-grid-layout/ "Curso Recomendado")

------------


### FLUJO NORMAL DEL DOCUMENTO: DISPLAY BLOCK, INLINE E INLINE-BLOCK

**Elementos inline:** Son los elementos que comúnmente conocemos como horizontales, aunque realmente este concepto puede cambiar si cambiamos el modo de escritura

**Elementos block: **Son los elementos que comúnmente conocemos como verticales, aunque realmente este concepto puede cambiar si cambiamos el modo de escritura


------------

### CONTEXTOS DE FORMATO: FORMATO DE CONTEXTO DE BLOQUE (BFC)

**Block formatting context (BFC)**

Es el layout interno de un elemento, que se comporta de manera independiente a como se comporta el resto de la página

Si bien maneja la estructura interna de un elemento, utilizando position se puede sacar al elemento del flujo normal del documento, haciendo que este se reordene de una forma distinta

**¿Que pasa con flexbox y grid?**

Ambos formatos nacieron con la intensión de facilitar el diseño de la página. Mientras flexbox se basa en un formato donde se le da flexibilidad a los elementos y al contenedor, grid adquiere un formato de cuadricula** realmente facil de ordenar**

**¿E Inline-block?**

Inline-block es bastante facil de entender. Consta en una fusión de ambas partes, donde al igual que inline-flex e inline-block, externamente el elemento se situa de forma inline, pero por dentro puede adoptar propiedades block como width, left, etc…

**Sobre flow-root**

Personalmente no entendí cual es la funcionalidad de flow-root. Tuve que buscar en documentación y aun así no me quedó del todo clado su uso, pero entre sus caracteristicas resetea el flujo del documento, permitiendo posicionar correctamente los elementos float (que, al ser float, se descolocan del flujo, y al resetearlo lo vuelve a ubicar) esto es genial para casos donde tenes que usar elementos flotantes y no queres que se te desordene toda la caja


------------

### POSICIONAMIENTO

<img src="https://static.platzi.com/media/user_upload/understanding_zindex_04-53c16f18-3e1e-4d2c-b273-7b8ad186e30e.jpg" alt="posiconamiento z-index">

DIV #4 es renderizado debajo de DIV #1 porque el z-index (5) de DIV #1 es válido dentro del contexto de apilamiento del elemento raiz, mientras que el z-index (6) de DIV #4 es válido dentro del contexto de apilamiento de DIV #3. Así que DIV #4 está debajo de DIV #1, porque DIV #4 pertenece a DIV #3, que tiene un valor z-index menor.

Por la misma razón DIV #2 (z-index 2) es renderizado bajo DIV#5 (z-index 1) porqué DIV #5 pertenece a DIV #3, que tiene un valor z-index mayor.

El valor z-index de DIV #3 es 4, pero este valor es independiente del z-index de DIV #4, DIV #5 and DIV #6, porque pertenece a un contexto de apilamiento diferente.


------------



[========]

## FLEXBOX O CSS GRID

### DIFERENCIAS ENTRE FLEXBOX Y CSS GRID

**Flexbox**

- Es un método que puede ayudar a distribuir el espacio entre los ítems de una interfaz y mejorar las capacidades de alineación
- Es unidimensional ⇒ Una sola dirección

**CSS Grid**

- Es un sistema de diseño que permite al autor alinear elementos en columnas y filas
- Es bidimensional

<img src="https://miro.medium.com/max/880/1*L-udJojk8cUUCXMyKB1IKQ.png" alt="differences flexbox vs grid">

------------


### SIMILITUDES ENTRE FLEXBOX Y CSS GRID

Flexbox y CSS Grid comparten dos características las relaciones padre e hijo y los ejes de alineamiento que tiene cada una


------------

### ¿PUEDO TRABAJAR CON FLEXBOX Y CSS GRID AL TIEMPO?

Si.

------------
### DINÁMICA: ¿QUÉ USARÍAS? (PARTE 2) + RETO

<img src="https://static.platzi.com/media/user_upload/dinamica-60378185-e048-44c6-bb6f-382a2f49187d.jpg" alt="reto">

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Dinamica ¿Que usarias?</title>
    </head>
    <style>
    
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    html{
        font-size: 62.5%;
    }
    
    body {
        background-color: #2e2ec2;
        color: white;
        font-size: 1.6rem;
    }
    
    .card{
        padding: 10px;
        width: 350px;
        height: auto;
        background-color: #101216;
        margin: auto;
       
        box-shadow: 0 0 12px 4px rgba(55, 55, 55, 0.5);
    }
    
    .header{
        display: grid;
        grid-template-areas: 
                            "img title"
                            "img subtitle";
        height: auto;
        width: 100%;
        padding: 10px;
        align-items: center;
      
    }
    
    
    .header__img{
        grid-area: img;
        width: 50px;
        height: 50px;
        border-radius: 50%;
       justify-self: center;
    
    }
    
    .header__title{
        margin: 10px;
        grid-area: title;
    }
    
    .header__subtitle{
        grid-area:subtitle;
        font-size: 1.4rem;
        margin: 10px;
    }
    
    .main{
        /* display: flex; */
    }
    
    .main__img img{
        display: block;
        width: 100%;
        height: auto;
       
    }
    
    .main__paragraph p {
        margin-top: 10px;
        padding-top: 10px;
    }
    
    .footer{
        display: flex;
        margin-top: 30px;
        justify-content: space-between;
    }
    
    .footer .container__footer {
        width: 50%;
        display: flex;
        justify-content: space-evenly;
    
    }
    
    .footer .container__footer button{
        background-color: azure;
        font-size: 1.4rem;
        border: none;
        padding: 10px;
        border-radius: 5px;
    
    }
    
    .container__footer--icons{
        display: flex;
        justify-content: space-evenly;
        width: 25%;
    }
    
    
    
    
    
    </style>
    <body>
    <article class="card">
    
    
        <header class="header">
            <img class="header__img" src="./plane.jpg" alt="plane">
            <h1 class="header__title">
                El titulo va aqui
            </h1>
            <h2 class="header__subtitle">
                Segundo Titulo
            </h2>
        </header>
        
        
       <main class="main">
            <section class="main__img">
                <img src="./aircraft.jpg" alt="aircraft">
            </section>
            <section class="main__paragraph">
                <p>
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rem dolore veniam commodi velit quae laborum quas corrupti facilis vitae provident! Itaque fuga, unde recusandae accusantium aliquid illo sunt dicta minima!
                </p>
            </section>
        </main>
        
         
        <footer class="footer">
            <div class="container__footer">
                <button class="container__footer--button-one">
                    Action 1
                </button>
                <button class="container__footer--button-second">
                    Action2
                </button>
            </div>
            <div class="container__footer--icons">
                <span class="icon__heart">
                    <img src="./SVG/heart.svg" alt="">
                </span>
                <span class="icon__share">
                    <img src="./SVG/shuffle.svg" alt="">
                </span>
            </div>
        </footer> 
    </article>
    </body>
    </html>


------------

### ¿CUÁNDO USAR FLEXBOX Y CUÁNDO USAR CSS GRID?

Flexbox = componentes de escala pequeña.
Grid = componentes de escala más grandes como layout.

Al momento de implementar, crear tareas para la creación de componentes en este ejemplo serían:

1. Crear la grid principal.
2. Crear la grid de los hijos.
3. Crear 3 tipos de cards
4. Ubicar cards


------------

## MODEREN LAYOUT CON CSS GRID

### ¿QUÉ SON LOS MODERN CSS LAYOUTS?

El layout es el diseño que tenemos, de como colocamos nuestros elementos su organización. Modern CSS layouts es algo que tiene 10 años, igual usaban HTML5 y CSS3, y en 2010 había ciertas características que se requerían como:

- Progresivamente mejorando: Una base solida de CSS y con base se pueda construir lo demás.
- Adaptable a diversos usuarios: Que se pueda ver en diferentes tipos de navegadores y que sea responsive.
- Modulares y eficientes: Tener pequeños componentes y de ahí fueran creciendo los demás y se puedan reutilizar. Antes usaban frameworks de Object Oriented para CSS para tener un código rápido, fácil de mantener y basado en estándares.
- Tipográficamente ricos: Había muchas tipos de tipografías.

Las cosas que querían lograr antes es igual a lo que queremos ahora, la idea de CSS grid lleva años desarrollándose la idea de tener un layout basado en filas y columnas y en 2017 esa idea se concreto. Queríamos tener la misma estructura para layouts pero las cosas van evolucionado y mejorando y ahora podemos tener mejores y más sencillos layouts.

------------

### PATRONES PARA USAR COMO PUNTO DE PARTIDA

[Patrones](https://gridbyexample.com/patterns/ "Patrones")

------------

### LAYOUTS

- Super Centered

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Super centered</title>
            <link rel="stylesheet" href="style.css">
        </head>
        <body>
            <div class="parent">
                <div class="child">:)</div>
            </div>
        </body>
        </html>
        CSS
        
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }
        
        html {
            font-size: 62.5%;
        }
        
        .parent {
            height: 100vh;
            width: 100vw;
            display: grid;
            place-items: center;
            background-color: aqua;
        }
        
        .child {
            height: 50px;
            width: 20px;
            display: grid;
            place-items: center;
            background-color: blueviolet;
            font-size: 1.2rem;
            font-weight: bold;
        }
    

- The Deconstructed Pancake

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Deconstructed pancake</title>
            <link rel="stylesheet" href="style.css">
        </head>
        <body>
            <div class="parent">
                <div class="child">1</div>
                <div class="child">2</div>
                <div class="child">3</div>
            </div>
        </body>
        </html>
        CSS
        
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }
        
        html {
            font-size: 62.5%;
        }
        
        .parent {
            height: 100vh;
            width: 100vw;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .child {
            flex: 0 1 300px;
            display: grid;
            place-items: center;
            margin: 15px;
            background-color: aqua;
            font-size: 1.2rem;
            font-weight: bold;
        }
   


- Sidebar Says


        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Sidebar Says</title>
            <link rel="stylesheet" href="style.css">
        </head>
        <body>
            <div class="parent">
                <div class="sidebar">min: 150 / max: 25%</div>
                <div class="element">Takes the second grid position</div>
            </div>
        </body>
        </html>
        
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }
        
        html {
            font-size: 62.5%;
        }
        
        .parent {
            height: 100vh;
            width: 100vw;
            display: grid;
            grid-template-columns: minmax(150px, 25%) 1fr;
        }
        
        .sidebar, .element {
            display: grid;
            place-items: center;
            font-size: 1.2rem;
            font-weight: bold;
        }
        
        .sidebar {
            background-color: yellow;
        }
        
        .element {
            background-color: palevioletred;
        }
    

- Pancake Stack



- Classic Holy Grail Layout

  	  <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Holy Grail</title>
            <link rel="stylesheet" href="style.css">
        </head>
        <body>
            <div class="parent">
                <header>Header</header>
                <section class="left-sidebar">Left Sidebar</section>
                <main>Main</main>
                <section class="right-sidebar">Right Sidebar</section>
                <footer>Footer Content</footer>
            </div>
        </body>
        </html>
        
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }
        
        html {
            font-size: 62.5%;
        }
        
        .parent {
            height: 100vh;
            width: 100vw;
            display: grid;
            grid-template: auto 1fr auto / auto 1fr auto;
        }
        
        header, main, .left-sidebar, .right-sidebar, footer {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        header {
            grid-column: 1 / 4;
            background-color: yellow;
        }
        
        .left-sidebar {
            grid-column: 1 / 2;
            background-color: coral;
        }
        
        main {
            grid-column: 2 / 3;
            background-color: palevioletred;
        }
        
        .right-sidebar {
            grid-column: 3 / 4;
            background-color: greenyellow;
        }
        
        footer {
            grid-column: 1 / 4;
            background-color: cadetblue;
        }
    
------------

### Layouts: 

- 12-Span Grid
- RAM (Repeat, Auto, MinMax)
- Line Up
- Clamping My Style
- Respect for Aspect

<img src="https://static.platzi.com/media/user_upload/layouts-c5ca7b87-9555-433f-83dc-7c30b57f138f.jpg" alt="layouts">

------------

[========]

## DISEÑO WEB PARA DESARROLLADORES

### DINÁMICA: NO PUEDO DEJAR DE VER

Una serie de retos para entrenar la vista de maquetador

[Cant unsee](https://cantunsee.space/ "Cant unsee")


------------

### DESIGN SYSTEM Y DETALLES VISUALES A TENER EN CUENTA

Lecturas recomendadas: 

[Shopify](https://polaris.shopify.com/design/design "Shopify")

[Tailwinds](https://tailwindcss.com/docs "Tailwinds")

[Design Tokens](https://css-tricks.com/what-are-design-tokens/ "Design Tokens")

------------

### TENDENCIAS DE DISEÑO UI/UX: FASE DE INSPIRACIÓN Y CREATIVIDAD

Tips:
• Jerarquía
• Contraste
• Proximidad
• Balance
• Responsive design
• Ilustraciones animadas
• Garantizar performance
• Micro interaciones
• Realidad aumentada y realidad virtual
• Neo morfismo
• Asymmetrical layouts
• Storytelling

[Neomorfismo](https://neumorphism.io/#e0e0e0 "Neomorfismo")

[Tendencias UX](https://trends.uxdesign.cc/ "Tendencias UX")


------------

### WIREFRAMES Y COMUNICACIÓN VISUAL SIMPLE, INTUITIVA Y ATRACTIVA


------------

### FIGMA PARA DEVS: AUTO LAYOUT Y NEUMORPHISM (PARTE 1)

[Twitter figma](https://twitter.com/figmadesign/status/1329455521355730945 "Twitter figma")

[Figma](https://www.figma.com "Figma")

[Inspiracion reproductor de musica](https://co.pinterest.com/pin/576671927272675751/ "Inspiracion reproductor de musica")

[Neumorfismo](https://medium.com/@artofofiare/neumorphism-the-right-way-a-2020-design-trend-386e6a09040a "Neumorfismo")

El reto consiste en crear en Figma un layaout con las caracteristicas de neumorfismo de un reproductor de musica

Asi que hay que construir el frame con unos 4 rectangulos adentro. 
1 de footer
1 de header
1 de main section
1 de botones

En el de main section colocar cuadros que simulen la imagen de la cancion
En la seccion de botones crear 5 elipses.

Uno mas grande al centro y las otras dos a cada lado.

------------

[========]


## DEL DISEÑO AL CODIGO

### PRIMEROS PASOS Y ESTRUCTURA INICIAL

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Primeros pasos y estructura inicial</title>
    </head>
    <body>
        <header class="header">
            
        </header>
        <section class="cards">
    
        </section>
        <section class="progress__bar">
    
        </section>
        <footer class="buttons">
            
        </footer>
    </body>
    </html>
	

------------

### UBICACION Y CREACION DE ELEMENTOS

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Primeros pasos y estructura inicial</title>
    </head>
    <style>
    
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100&display=swap');
    
    :root {
      --blue: #EAF0F8;
    }
    
    body {
      margin: 0;
      background: var(--blue);
      font-family: 'Roboto', sans-serif;
    }
    
    .wrapper{
        display: grid;
        grid-template-rows: 60px 300px auto auto;
        height: 100vh;
    }
    
    .header{
        /* border: 1px solid red; */
        display: flex;
        justify-content: center;
        align-items: center;
    }
    
    .cards div{
        margin: 20px;
        width: 250px;
        height: 250px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        background: #dee0e8;
        box-shadow:  5px 5px 0px #595a5d,
                 -5px -5px 0px #ffffff;
    }
    
    </style>
    
    
    <body>
    <div class="wrapper">
    
        <header class="header">
            <p>Playing Now</p>
        </header>
        <section class="cards">
            <div>
    
            </div>
        </section>
        <section class="progress__bar">
    
        </section>
        <footer class="buttons">
    
        </footer>
    
    </div>
    </body>
    </html>


------------

[========]


## EL FUTURO DE CSS GRID

### CSS SUBGRID

- Experimental
- Soportado solo por Firefox actualmente: mar/2021

------------

### NATIVE CSS MASSONRY LAYOUT

Basicamente un modelo de grillas como pinterest.

Masonry, en español Mampostería. Se llama mampostería al sistema tradicional de construcción que consiste en erigir muros y paramentos mediante la colocación manual de los elementos o los materiales que los componen (denominados mampuestos), que pueden caracterizarse por estar sin labrar.

<img src="https://www.aparicio-partner.com/wp-content/uploads/2017/05/foto_sassi_rocce_02-1024x675.jpg" alt="monssonry layout">

[Lecturra son monssory](https://www.smashingmagazine.com/native-css-masonry-layout-css-grid/ "Lecturra son monssory")

------------

### CSS FEATURE QUERIES: @SUPPORTS

Por ejemplo:

    @supports (grid-template-columns) and (not (subgrid)) {
    	// Creas las columnas del padre dentro del hijo
    }
    
    //Si soportas grid-template-columns y no soportas subgrid, interpreta el contenido de las llaves
    
    @supports (subgrid) {
    	grid-template-columns: subgrid;
    }
    //Si soportas subgrid interpreta el contenido de las llaves

[Suports](https://css-tricks.com/get-ready-for-display-contents/ "Suports")

### TIPS PARA SEGUIR APRENDIENDO Y MANTENERSE AL DÍA

- Seguir personas que pertenezcan al CSS Work Group
	- Rachel Andrews
	- Jen Simmons
	- Adam Argyle
- Leer Mucho
	- Medium
	- MDN Mozilla Developers
	- Smashing Magazine
- Tener paciencia
- Mucha practica


[========]


