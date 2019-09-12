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


## Añadiendo características dedicadas a pantallas pequeñas

### Videos HTML5

Como sabes, los videos son contenidos cada vez más comunes e incluso necesarios en las web sites.

Por esta razón, en esta clase aprenderás a incluir un video en tu proyecto y, por lo tanto, lo modificarás para convertirlo en un material responsivo, es decir, que sea coherente con tu trabajo de Responsive Design.

Para aprender esto es necesario que elijas cualquier video que tengas en su formato original y sigas las indicaciones que tu profesor, Leonidas Esteban, realizará a lo largo de la clase.

Las dos foras de insertar un vídeo en 
- Vídeo en HTML
- Vídeo insertado

Ver más en [Usando audio y video con HTML5](https://developer.mozilla.org/es/docs/Web/HTML/Usando_audio_y_video_con_HTML5)


### Video insertado

En esta clase aprenderás a implementar videos responsive en tu proyecto, originarios o alojados en otras plataformas (como youtube y/o vimeo). Por este motivo trabajarás con la etiqueta iframe.

Ésta etiqueta hará posible que el video que insertes tenga la posibilidad de adaptarse a distintas formas de visualización, aunque, a pesar de ellas, aprenderás cuáles son las diferencias entre usar un video inserto y hacerlo desde html5.

- **iframe** La etiqueta permite insertar contenido desde cualquier website al nuestro.

- **Para video en relación 19:9**
`height*100/width`

Para vídeo **vertical** se hace
`width*100/height`


### Fuentes de iconos

Para íconos personalizados podemos traerlos desde IcoMoon.io

Todo menú necesita de la presencia de iconos, por este motivo, en esta clase aprenderás sobre las fuentes de iconos y las aplicarás en la realización del menú de tu proyecto.

En este abordaje a las fuentes de iconos, conocerás la plataforma icomoon.io, en ella podrás importar o añadir familias de iconos, desde tu computador o desde el sistema.

Posteriormente, llevarás los archivos que selecciones a tu editor de código, allí trabajarás sobre ellos con la etiqueta @font- face, que acogerá a otros atributos como font- family, font- style y font- weigth, font- variant, entre otras.

El **tag** `<i></i>` se recomienda para insertar íconos


### Añadiendo un menú de hamburguesa

En esta clase convertirás el ícono que has elegido según las fuentes de íconos y le destinarás una función, es decir, le adjudicarás un “call to action” o llamado a la acción. Así, tu usuario sabrá cómo relacionar el ícono a la función que necesita realizar. En conclusión, durante la clase, Leonidas te enseñará diversas técnicas para desarrollar tu menú de hamburguesa o menú desplegable de múltiples opciones, en la página web que estas desarrollando, en estas formas trabajarás sobre las medidas, los colores, el background color, el borde, el display y, algo fundamental, las posiciones de css que ya aprendiste en la clase correspondiente a este tema.

- ¿Qué propiedad se desbloquea luego de asignar un position diferente de static en un elemento?

top, bottom, right, left y x-index


## Posicionando el menú

Antes de que tu menú tenga elementos que permitan la interactividad, es necesario definir sus posiciones y ordenamientos desde tu editor de código. En esta clase definirás los tamaños de tu menú, de los textos y, especialmente, trabajarás sobre sus estilos. Estos estilos los irás comprobando en distintas opciones de visualización o tamaños de dispositivos, con el propósito de estar realizando un trabajo efectivo en cuanto al responsive design. No obstante, al finalizar verás que aun no tiene la posibilidad de aparecer y esconderse, según lo necesite tu usuario, por este motivo: te invitamos a ver la próxima clase en donde usarás elementos de javascript para brindarle otra experiencia, mucho más completa, a tus usuarios.

## Añadiendo Javascript para detección de eventos

La interactividad que necesitarás para tu menú, se concentrará en algunas acciones, la primera de ellas es la que sucede al cliquear sobre el botón o el icono.

Para lograr esto harás uso del lenguaje de programación JavaScript, recuerda que este lenguaje hace posible la codificación de experiencias interactivas en el desarrollo web (si te interesa, te recomendamos tomar el Curso de jQuery a JavaScript, y el curso de Fundamentos de JavaScript).

Algunas de las instrucciones de JS que aplicarás serán, console.log, document.querySelector, classList, variables (const nombre =), burgerButton, EventListener, entre otras.


## Media queries con JavaScript

En esta clase aprenderás a implementar media queries con JavaScript, para esto usarás instrucciones como window.matchMedia, console.log -nuevamente-, event, entre otros.

El propósito es que tu menú quede listo para ofrecer una experiencia interactiva y sea flexible en distintos dispositivos, es decir, que sea interactivo y responsivo.

De forma adicional, aprenderás a agregar y quitar listeners de tus eventos, pues no siempre son la mejor opción en la experiencia de navegación.


```js
window.matchMedia('screen and (mac-switdth: 767px)');
```

Con **window.matchMedia** invocamos una función de la API del navegador, que nos permite hacer una consulta a los medios, en este caso para el media query que hemos dispuesto para el tamaño del del ipad.


La funcionalidad que permite agregar la nteractividad al botón es la siguiente:

```js
const menu = document.querySelector('.menu');
    const burgerButton = document.querySelector('#burguer-menu');

    function hideShow(){
      if (menu.classList.contains('is-active')){
        menu.classList.remove('is-active');
      } else {
        menu.classList.add('is-active');
      }
      
    }

    const ipad = window.matchMedia('screen and (max-width: 767px)');

    ipad.addListener(validacion);

    function validacion(event){
      if (event.matches){
        burgerButton.addEventListener('click', hideShow);
      } else {
        burgerButton.removeEventListener('click', hideShow);
      }
    }
```

## Creando un servidor de archivos estáticos con Node

En esta clase verás qué diferencias hay entre el navegador y la visualización del teléfono, a lo que se le conoce como remote debugging y de lo que aprenderás más adelante.

Por ahora, aprenderás a realizar un servidor de archivos estáticos con Node, esto te permitirá contar con las herramientas necesarias para trabajar sobre el remote debugging en distintos dispositivos. Así que, en primer lugar vas a descargar el software de Node, que te permitirá crear los archivos estáticos.

- [Static Server](https://www.npmjs.com/package/static-server)

Para ello usamos el comando
- Instalamos nodeJS y npm
 - `npm -g install static-server`, Para instalar el módulo. Damos permisos de administrador **sudo** para _linux_ y _mac_
- Vamos a la carpeta de nuestro proyecto
- Ejecutamos el comando **`static-server`** (Apagamos el servidor con **ctrl + c**)
- Buscamos la IP de la red local, viendo las propiedades de la conexión


## Remote Debugging en iOS

En este momento ya debes poder acceder a tu proyecto para depurarlo desde tu teléfono móvil.

En esta clase vas a aprender a trabajar sobre el rendimiento de la interfaz que ves en la navegación, de esta manera, aprenderás a corregir bugs y trabajar desde el inspector de elementos de tu celular, ya que es posible que accedas a él y trabajes en él. Finalmente aprenderás a configurar el remote debugging para iOS.

## Remote Debugging en Android y puliendo últimos detalles

Así como aprendiste a configurar el remote debugging para iOS, en esta clase aprenderás a configurarlo para dispositivos Android. Para aprender a hacerlo, debes tener conectado tu teléfono a tu computador vía usb y activar el menú de desarrollador -el cual se encuentra en la configuración-; al activarlo debe aparecer un menú adicional desde el cual podrás utilizar el inspector de elementos en tu computador, desde el explorador que tengas (que para esta ocasión será Google Chrome). Desde este lugar podrás modificar los diversos elementos de tu proyecto, aplicando las herramientas y conocimientos que ya dominas hasta el momento. Por último, ¡pulirás los detalles finales de tu proyecto!


- Para depurar en Android, debemos seguir los siguientes pasos.
  - Activar las opciones de desarrollador en android
  - Aceptar la vinculación del teléfono con la computadora.
  - Acceder a la ruta `chrome://inspect` en **chrome**
  - Ver el dispositivo, verificar el sitio wen y realizar las modificaciones requeridas

