# CURSO HTML Y CSS DEFINITIVO

## Por Edier Dario Bravo Bravo

# Estructura basica de HTML

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


