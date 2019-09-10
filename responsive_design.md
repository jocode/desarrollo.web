# Responsive Design

## Conceptos elementales de Responsive Design

Son todas las técnicas que usamos para adaptar nuestras aplicaciones web a la mayor cantidad de pantallas.

**Principios del Responsive Design**
- Mostly fluid
- Colocación de columnas (Google)
- Layout shifter
- Tiny tweaks
- Off canvas.

Los sitios web responsives (Para inspiración y guías) ver https://mediaqueri.es/

- **viewport** El área visible del navegadpr
- **portrait - landscape** 
  - Vertical
  - Horizontal
- **Mobile First** Empezar un website desde la menor resolución soportada
- **Desktop First** Empezar un web site desde la mayor resolución soportada

- **¿Cuál es mejor?** Técnicamente Mobile First


## Meta viewport

La etiqueta meta viewport es una etiqueta de metadatos que te ayudará a configurar tu website para que sea visible en dispositivos de menor tamaño.

Uno de los objetivos principales al usar esta etiqueta será que conserves la legibilidad de tu página web, al variar el escalado de tus contenidos.

## Medidas relativas útiles en Responsive Design

Lo primero que debes tener en cuenta es que estas medidas son maleables, en la medida en que dependen de su fuente de origen o medida madre. Entre ellas se encuentran:
- **porcentaje** (longitud referente al tamaño de los elementos padre)
- **em** (unidad relativa al tamaño de fuente especificada más cercano)
- **rem** (unidad relativa al tamaño de fuente especificada en el ancestro más lejano, como html o body)
- Tamaños del **viewport vw/vh** (longitud relativa porcentual con respecto al viewport).


## Media queries

Para que logres los resultados que deseas en tus proyectos, es necesario cambiar ciertas propiedades para modificar el tamaño de los textos, contenidos y hojas de estilo; la manera de hacer esto es el media queries.

El **media queries** es un *módulo de css que hace posible al responsive design*, éste existe desde el 2010 y se encarga de adaptar la representación del contenido a características del dispositivo.

- Un media query se compone de un media **type** y una o más condiciones

```css
@media media type and (condición){

}
```

```css
@media screen and (max-width: 768px){

}
```
*Todas las pantallas con un ancho inferior o igual a 768px cumplen esa condicion*

```css
@media screen and (max-width: 768px) and (min-width: 480px){

}
```
*Todas las pantallas con un ancho de 480px hasta 768px cumplen esta condición*


### Mobile First

- `@media screen and (min-width: 320px){}`
- `@media screen and (min-width: 480px){}`
- `@media screen and (min-width: 768px){}`
- `@media screen and (min-width: 1024px){}`

Usa **min-width** = desde

### Desktop First

- `@media screen and (max-width: 1024px){}`
- `@media screen and (max-width: 768px){}`
- `@media screen and (max-width: 480px){}`
- `@media screen and (max-width: 320){}`

Usa **max-width** = hasta


## Formas de incluir media queries

El primer paso para lograr esto será realizar una nueva hoja de estilos en tu proyecto, ésta debe contar, en primer lugar, con la etiqueta link; harás uso de la aplicación de medidas para la pantalla, bordes y colores, entre otras características.

Hay 3 formas de incluirse los media querys
- Usando la etiqueta link, usando la propiedad **media**
  - `<link rel="stylesheet" href="media.css" media="screen and (max-width: 768px)"/>`

- Incluyendo la condición en el archivo css

```css
@media screen and (max-width: 768px){
  body {
    border: 10px solid green;
  }
}
```

- Usando el tag **style** dentro del html y escribiendo los estilos ahí

```html
<style>
    @media screen and (max-width: 768px) {
      body {
        border: 10px solid blue;
      }
    }
  </style>
```


> A los media query puestos para cada resolución se les denomina **break points**


## Diseño elástico con max-width y flex-wrap

Como te habrás dado cuenta tu proyecto está desordenado aunque carga en el viewport. Por esta razón en esta clase aprenderás a ordenar tu proyecto por medio del uso de contenedores flexibles, que varíen su tamaño según la amplitud con la que cuentan en diversos dispositivos y permitan una óptima visualización.

Por otro lado, para hacer esto posible, aprenderás a aplicar las etiquetas de max-width y flex- wrap; éstas también te ayudarán a evitar que tu usuario necesite navegar la página de forma horizontal, pues la información se organizará en forma vertical para facilitar la experiencia.

## Ajustando el header

En esta clase aprenderás a trabajar sobre tu proyecto, sección por sección.

La primera de ellas será el header. Para esto inspeccionarás los elementos del header y su menú (alto, contenedor, ancho máximo, media queries, alto…).

Adicionalmente, aplicarás etiquetas y elementos como flex, padding, width, display, display blog, justify-content, align-items, header ol li, figue, images, menús, entre otros.

> Siempre es mejor tener las cosas en **diplay: block** y en **width: auto** porque da mucho mejor rendimiento en el render del navegador. (Es mejor ancho auto que ancho 100%... ¡Toda la vida!)

- **Hacer una imagen responsive**
 Se define que el máximo ancho sea el 100% del ancho del elemento padre **max-width: 100%**

- **IMPORTANTE**
 Esta es una excelente línea de codigo en CSS, mediante calc, calculamos el ancho de la fuente dependiendo del viewport. Donde 19 es el tamaño maximo, en desktop y 14 es el minimo para pantallas pequeñas. Lo mas interesantes es que sus valores varian segun su viewport, osea que toma todos los valores entre 14 y 19
**font-size: calc(14px(valor minimo) + (19(valor máximo) - 14) * ((100vw - 300px) / (1600 - 300)))**;



## Ajustando la sección de contacto y footer

Es hora de trabajar sobre la sección de contacto y el footer de tu proyecto, por lo que en esta clase aprenderás a modificar ambas secciones.

En el trabajo sobre estas secciones modificarás sus elementos de contacto, padding, el modelo de caja (aprenderás que en algunas ocasiones es necesario eliminarlo y rehacerlo) el container y su respectivo padding.

Y por último, también trabajarás sobre los elementos propios de los botones que se encuentran en estas secciones.


Para arreglar el **margin collapsing** podemos arreglarlo usando dos formas distintas
- **padding: 1px;**
- **border: 1px solid transparent;**

## CSS positions

En tu proyecto, al probarlo en distintos dispositivos, te darás cuenta de que no solamente sus elementos y contenidos deben tener la propiedad de cambiar sus tamaños y condiciones para hacerse elementos de una buena visualización; sino que, además, hay unos ciertos contenidos que permanecen constantemente en el espacio de visualización, a pesar de que tu usuario realice scroll en la página.

Estos elementos te darán cuenta de uno, entre los varios tipos, de posiciones que permite CSS. Por esta razón, durante esta clase conocerás cuáles son las distintas posiciones (estática, relativa, absoluta, fixed y sticky) sobre las que podrás trabajar, aplicándolas a tu proyecto. Material de trabajo de esta clase: 

[CSS Positions](https://codepen.io/LeonidasEsteban/pen/VGWzWK)

Las posiciones nos permitirán superponer los elementos, a forma de capas.

- **Tipos de posiciones `position: static;`**
  - static (Por defecto)
  - relative
  - absolute
  - fixed
  - sticky

Cuando el tipo de posición es **diferente a static** se desbloquean dos propiedades
- **z-index** Se coloca encima de otro elemento (Como capas)
- **top right botton left** Mover el elemento dentro del contenedor

Al modificar esto nunca cambia la posición de los siguientes elementos.

La posición **absolute** depende de la **relative**, por esa razón si queremos colocar un elemento dentro de la absoluta, debemos definir el contendor como **position: relative**


- **position: fixed**

```css
p {
  position: fixed;
  top: 0;
}
```
El elemento se pone encima de todo y se mantiene fijo.

- **position: sticky**

Cuando se define la posición sticky hay que definirle con respecto a quien se va a pegar

```css
.sticky {
  position: sticky;
  top: 0;
  background: rgba(0,0,0,.5);
}
```

### Positions

Cuando asignamos un valor a la propiedad position que no sea **static** (**por defecto**), se desbloquean 2 propiedades, las cuales son `z-index` y (`top, right, left y bottom`).

- **static**: Posición que llevan todos los elementos por defecto.

- **relative**: El elemento se mueve (n) espacios desde la dirección desde donde se encontraba originalmente, salvaguardando también el espacio donde se encontraba. Cuando aplicas un valor positivo, se mueve en dirección contraria a este y viceversa.

- **absolute**: Se sale del elemento en el que se encontraba originalmente y se ubica de manera absoluta y relativa con relación al elemento mas cercano que tenga la posición relativa o por defecto con el último elemento de html (el cual puede ser body o html por defecto).

- **fixed**: Se queda fijo en un lugar especifico del viewport que se le indique.

- **sticky**: Permanece en un lugar asignado y cuando se hace scroll se queda fijo en un lugar en especifico hasta que se haga scroll contrario.