# CURSO HTML Y CSS DEFINITIVO

## Por Edier Dario Bravo Bravo

# Estructura basica de HTML

Enlaces importantes

[Notas de otro estudiante](https://johncardenasp.notion.site/Curso-definitivo-de-HTML-y-CSS-7196d473c6b046d2b8de4a0edaa82dc6)

[Tabla de etiquetas](https://allthetags.com/)

[HTML: Lenguaje de etiquetas de hipertexto](https://developer.mozilla.org/es/docs/Web/HTML)

[Referencia de Elementos HTML](https://developer.mozilla.org/es/docs/Web/HTML/Element)

## Etiquetas de HTML

- article: diferencia partes del contenido que pueden vivir por sí mismas.

- nav: para hacer menús de navegación.

- aside: contenido menos relevante, como publicidad, etc.

- section: sirve para diferenciar las secciones principales del contenido.

- header: cabecera del documento.

- footer: pie de página del documento.

- h1 - h6: títulos de nuestro sitio web.

- table: tablas de contenidos, similar a la estructura de las hojas de calculo.

- ul y ol: listas de items.

- div: cualquier división para organizar el contenido.

- h1 a h6: son etiquetas para indicar títulos con un estilo que destaca del resto.

- article: es la parte de nuestro contenido que puede vivir por sí mismo. Pueden haber tantos artícle como proyectos o eventos tenga nuestro portafolio.

- p: define el texto de un párrafo.
small: aplica una apariencia de texto reducido en tamaño.

- strong: aplica al texto un formato de negritas.

- a: corresponde a un ancla o enlace a una url interna o externa del documento.

- img: con esta etiqueta podemos enlazar imágenes en el documento.

- figure: le da un contexto semántico a las imágenes.

![Tabla etiquetas HTML](images/tablaetiquetas.webp)

## Estructura basica  de HTML

```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="description" content="Esta pagina tendra informacion de gatos" />
    <meta name="robots" content="index,follow" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titulo</title>
    <link rel="stylesheet" href="./css/style.css">
\</head>

\<body>
  <header> <!--Sección superior de nuestro website--> 
    <nav></nav> <!--Sección de navegación de nuestro website, siempre dentro del header-->
  </header>

  <main> <!--Main es el contenido central de nuestro website, "la parte del medio"-->
    <section> 
      <!--Nuestro website puede estar divido por secciones, por ejemplo platzi tiene 3: El navegador de cursos y rutas, el feed y nuestras rutas de aprendizaje-->
      <article>
        <!--Contenido independiente de la página. Es reutilizable-->
      </article>
    </section>
    <ul> <!--Lista desordenada: Sin numerar-->
      <li><!--Item List. Elementos de la lista--></li>
    </ul>
    <ol></ol> <!--Lista ordenada: Numerada-->
  </main>

  <footer> <!--Sección final de nuestro website-->
  </footer>

  <p>Soy un texto</p> <!--Párrafo, texto-->

  <h1>Soy un titulo</h1> 
  <!--Títulos, muestran el texto más grande y con negrilla. Existen desde el h1 al h6-->

  <a href="#">Soy un link</a>
  <!--Enlaces/links que nos permitirán movernos entre páginas.-->
</body>

```

## Multimedia en HTML

#####  Imagenes

Existen imagenes sin perdida y con perdida:

- Sin perdida: la imagen no pierde imagen, son pesadas, las paginas demoran en cargar. (GIF, PNG 8, PNG 24, SVG)

- con perdidas: las imagenes pierden calidad pero el navegador carga rapidamente, son mas pequeñas. (JPG, JPEG)

El tamaño optimo de una imagen es de 70KB 

- [TinyPNG](https://tinypng.com/) mejora el tamaño de la imagen 

- [Verexif](https://www.verexif.com/) retira metadatos de las imagenes

[Pexels](https://www.pexels.com/es-es/) Para descargar imagenes en diferentes tamaños

###### Implementacion

figcaption: permite colocar descripcion a la imagen

```
<figure>
    <img src="lago.jpg" alt="Lago">
    <figcaption>Lago</figcaption>
</figure>
```

#####  Videos

- #t=3,8 permite reproducir del segundo 3 al segundo 8

- controls permite colocar los controles de pause, siguiente, ...

- preload="auto" permite cargar el video antes que la pagina termine de cargar

```
<video src="./video.mp4#t=3,8" controls preload="auto"></video>
```

Si el navegador no puede leer algun formato se puede hjacer de la siguiente forma para que alguno de los disponibles sea leido

```
<video controls preload="auto">
    <source src="./video.mp4#t=3,8" />
    <source src="./video.m4v#t=3,8" />
</video>
```

## Formularios

##### text, date, time, calendar, submit

[Input](https://developer.mozilla.org/es/docs/Web/HTML/Element/input) y todas sus caracteristicas

Forma no esperada pero valida

- type: tipo de entrada

- placeholder: Permite mostrar que es lo que se espera escribir en la caja de texto

```
<div>
    <input type="text">
    <input type="text" id="nombre" placeholder="Nombre">
    <input type="date" id="inicio-platzi">
    <input type="time" id="horario">
</div>
```

Forma deseada y correcta

- span: pregunta o informacion del formulario

- autocomplete: autocompleta el formulario

- required: campo obligatorio

- type="datetime-local": fecha con hora

```
<form action="">
    <label for="pais">
        <span>Tu pais</span>
        <input type="text" name="pais" id="pais" autocomplete="country" required>
    </label>
    <label for="nombre">
        <span>Cual es tu nombre</span>
        <input type="text" id="nombre" placeholder="Nombre">
    </label>
    <label for="inicio-platzi">
        <span>dia que comensaste en platzi</span>
        <input type="date" id="inicio-platzi">
    </label>
    <label for="horario">
        <span>tu horario</span>
        <input type="time" id="horario">
    </label>
    <label for="calendar">
        <span>Tu Cumpleaños</span>
        <input type="datetime-local" name="calendar" id="calendar" autocomplete="postal-code" required />
    </label>
</form>
```

##### Select

Forma no deseada, no apta para el usuario
```
<select name="" id="">
    <option value="js">JS</option>
    <option value="html5">HTML5</option>
    <option value="ccs3">CSS3</option>
</select>
```

Forma deseada: te permite elegir entre una lista y si quieres escribir te sugiere la opcion mas recomendada

```
<input list="cursos">
<datalist id="cursos">
    <option value="js"></option>
    <option value="html5"></option>
    <option value="ccs3"></option>
    <option value="web standar"></option>
</datalist>
```

##### Button

value: texto que aparece en el boton

```
<input type="submit" value="Nombre">
```

type: tipo de boton

```
<button type="submit">Nombre boton</button>
```

# ESTILOS CSS

[mozilla.org](https://developer.mozilla.org/en-US/docs/Learn/CSS) [w3schools.com](https://www.w3schools.com/css/default.asp) enlaces importantes 

[](https://www.w3schools.com/css/default.asp)
Tener en cuenta los Flexbox y CSS Grid que sirve para alinear. CSS permite hacer animaciones y response (adaptar la pagina Web a cualquer tamaño de pantalla)

Tienen dos parametros:

- Selector:
    - por etiqueta:

        div
    {
    ...
    }

    - por ID:

        #identificador
    {
    ...
    }
    
    - por clase:

        .clase
    {
    ...
    }
    
    - por atributo:

        [width="500"]
    {
    ...
    }
    
- Propiedades: dan estilo a la pagina web


###### No olvidar el estilo general
```
* {
margin: 0;
adding: 0; 
box-sizing:border-box; 
}
```

##### Seudo clases (Agregar `:class`) 

Definen el estilo de un estado especial de un elemento

- Cambiar de color al tener el cursor encima

```
.main-nav__item a:hover {
    color:rgb(174, 0, 255);
}
```

- Cambiar color al dar click encima
```

.main-nav__item a:active {
    color: red;
}
```

##### Seudo elementos (Agregar `::element`) 

Definen el estilo de una parte especifica de un elemento

- Agrega **-** despues del elemento

```
.main-nav__item a::after {
    content: " -";
}
```

## Modelo de caja

Todo se trata de cajas a los que le puedo colocar estilos

- margin: espacio externo a la caja

- border: dorde de la caja

- padding: espacio interno de la caja

- content: contenido ya sea imagen, video, texto, ...

- width: largo del contenido

- height: alto del contenido

- top, bottom, left, right: para posicionar el contenido

Se recomienda hacer esta configuracion a todo 

`box-sizing:border-box` permite que no se haga scroll horizontalmente al agregar borde y padding, pero no aplica a el margin.

```
* {
  margin: "0";
  padding: "0";
  box-sizing:border-box;
}
```

## Herencia
 Las clases padres heredan sus caracteristicas a sus clases hijas
 
- inherit: valor en los atributos de css para que herede caracteristicas de la clase padre

## Importancia de propiedades CSS

1 mas importante, 3 menos importante

1. Estilos de navegador
2. Nuestros estilos
3. Nuestros estilos declarados con `!important`

## Especifidad

Las clases son genericas pero los id son unicos

1 mas especificos, 5 menos esfecifico. Entre mas especifico sera el estilo aplicado

1. `!important` es el mas importante **10000**

2. estilos enbebidos (estilos en la estiqueta `<style>` de html) **01000**

3. #id **00100**

4. .class **00010**

5. tag o selectores de html **00001**

Si tengo un estilo aplicado a #id y .class el codigo es **00110**, esto es mas importante que solo #id

## Orden de las fuentes

No es buena parctica utilizar **estilos enbebidos**, llamar estilos por **id** y usar **`!important`**

Si hay conflictos en estilos, siempre se toma el ultimo. El archivo .css se lee de arriba hacia abajo, los ultimos estilos pueden reescribir a los primeros en caso de conflictos

Por otra parte los estilos llamados por `<link>` se leen de la misma manera, si hay mas de un llamado a archivos .css, los ultimos reescriben a los primeros en caso de conflictos

## Combinadores

Nos permite combinar multiple selectores y crear mayor especicidad

##### Hermano cercano o adyacente

Aplica color red a **p** que este cercano (justo despues de **h2**) a **h2**
```
h2 + p {
    color: red;
}
```
##### Hermano general

Aplica color rojo a **p** que este al lado  de **h2**, no importa si no esta contiguo ya que todos son hermanos generales

```
h2 ~ p {
    color: red;
}
```

##### Hermano hijo

Aplica color rojo a **p** que sea hija directa de **div**

```
div > p {
    color: red;
}
```

##### Hermano desendiente

Aplica color rojo a **p** que este dentro de **div**

```
div p {
    color: red;
}
```

## Medidas

##### absolutas

- px

##### Relativas

El width siempre debe ser relativo para buenas practicas

- %
- em : elemento

    Toma un tamaño de fuente de 1.5 veces del tamaño de fuente heredado o padre directo
    ```
    .text-container {
        font-size: 1.5em;
    }
    ```
- rem (root em) : root elemento

    Toma un tamaño de fuente de 1 veces del tamaño de root
    ```
    p {
        font-size: 1rem;
    }
    ```

    Para que un rem sea 10px usamos
    ```
    html {
        font-size: 62.5%;
    }
    ```
- max-width / max-height
- min-width / min height

    El tamaño de la section es del 80% pero en ancho no crecera mas de 500px ni reducira menos de 320px
    ```
    section {
        width: 80%;
        min-width: 320px;
        max-width: 500px;
    }
    ```
- vw (viewport width)
- vh (viewport height)

    El main va a tener un ancho y altura del 100% de la pantalla
    ```
    main {
        width: 100vw;
        height: 100vw;
    }
    ```
## Position (static, absolute, relative, fixed, sticky)

Todas las etiquetas vienen por defecto en `position: static`, en este caso no podemos usar bottom, left and right.

En **absolute** el objeto pierde la posocion.

En **relative** podemos usar bottom, left and right.

## Display

`display: block` utiliza el 100% del espacio width

`dispaly: inline` si hay espacio lo coloca en linea. Ademas no permite colocar padding, ni margin en la parte de arriba y abajo, ni width, ni height ya que ocupa el espacio del contenido

`display: inline-block` si hay espacio disponible permite width, height, margin, padding ya que ocupa el espacio del elemento

**flex**

[flex csss](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) parametros de display:flex

justify-content: permite centar horizontalmente

flex-wrap: permite que cuando la pantalla es muy pequeña, el contenido baje

**Flexbox**

`align-items: center` alicia verticalmente al centro

`align-items: flex-end` y ` align-items: flex-start` alinian el contenido abajo y arriba respectivamente. 

`align-items: stretch` si no se coloca altura definida, el contenedor crece en altura del contenedor padre. El ancho esta limitado con el contenido de cada contenedor

`align-items: baseline` el contenedor se limita al contenido del mismo siempre y cuando no tenga altura ni ancho definido.

`border: 1` para el contenedor a la posicion 1, los contenedores sin la propiedad border pasa al inicio y de ahi empieza el orden.

`flex-grow: 1` el contenedor con esta propiedad crece 1 unidad mas, es decir crece el espacio sobrante.

`flex-basis: 30rem` ancho base para wrap, si el contenedor ya es mas pequeño que ese tamaño pasa abajo, siempre y cuando este activada la propiedad `flex-wrap: wrap`

## Variables

Las variables se decalran como se muestra a continuacion, siempre colocar dos guiones al inicio

```
:root {
    --primary-color: #003476;
    --secundary-color: #7274fc;
    --header-size: 4rem;
    --font: 1.8rem;
}
```

Para usarlas se usa: `var(--primary-color)`

## Font

[Google Fonts](https://fonts.google.com/) para descargar fuentes para tu proyecto

Existen fuentes genericas que son las que ya vienen incorporadas en el computador

- serif: time new roman, georgia
- sans-serif: helvetica, verdana
- cursive
- monospace: courier new, roboto mono

Se recomienda solo cargar una fuente en nuestro proyecto e importarlas siempre desde la etiqueta head

## Responsive Design

**Mobile First / Only**

[Learn Responsive Design](https://web.dev/learn/design/)

Se inicia siempore desde pantallas mas pequeñas a mas grandes. Se colocan al final del style.css y solo los estilos que se van a modificar

```
@media (min-width: 480px){
    ...
}

@media (min-width: 720px){
    ...
}

@media (min-width: 1024px){
    ...
}
```

Tambiuen se puede colocar en el head de HTML y es la mejor opcion. Igualmente se usa de menor tamaño de pantalla a mayor tamaño de pantalla

```
<link href="style.css" rel="stylesheet"> <!--Estilo pra mobile-->

<link href="tablet.css" rel="stylesheet" media="screen and (min-width: 768px)">
```

**Mostly Fluid**

Se trata de ir reacomodando el contenido de la pagina web segun el tamaño de la pantalla

**Column Drop**

Se basa en romper la columna e ir modificando los elementos segun corresponda a medida que aumenta el tamaño de pantalla

**Resposive Imagenes**

Carga una imagen diferente segun el width de la pantalla, colocar de mayor a menor width

```
<picture>
    <source media="(min-width:500px)" srcset="./3.jpg"/>
    <source media="(min-width: 00px)" srcset="./2.jpg"/>
    <img src="./1.jpg" alt="Img 1"/>
</picture>
```

## Label, Alt, Title

El **for** de la etiqueta **label** debe ser igual al **id** de la etiqueta **input** para que cuando le de click al contenido del **span** en la pagina web, te señale de una el campo donde debo ingresar el dato

```
 <label for="time-to-study">
    <span>¿En que horario estudias?</span>
    <input type="time" id="time-to-study">
</label>
```

**alt** permite colocar un texto que se mostrara cuando no carga la imagen y ayudar a personas con problemas de vision. **title** permite mostrar un texto cuando tengo el cursor sobre la imagen

```
<img 
src="./img.jpg" 
alt="Foto del atardecer en una ciudad" 
title="Foto del atardecer en una ciudad">
```



# Recomendaciones

- Un archivo por cada break point, un break point es un ntamaño especifico de pantalla en la cual deseo posicionar el contenido de mi pagina o aplicativo web. En [MyDevice](https://www.mydevice.io/) úedo ver los diferentes tamaños de dispositivos del mercado

- Siempre se debe usar textos con medidas relativas como lo es rem

Asi debe ser una pagina WEB

![modelo](images/htmlEsquema.png)

### Sigue aprendiendo  ❤️ Programar es mas que un estilo de vida
