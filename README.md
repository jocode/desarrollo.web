# Curso de desarrollo web

El desarrollo web tiene que ver con todo lo que percibimos a través del navegador: páginas, aplicaciones y sitios web como Facebook, Instagram y Twitter.

Para comprender cómo funciona internet necesitamos conocer tres grandes conceptos:

- Clients (clientes): son los dispositivos a través de los cuales accedemos a los sitios web: un computador desktop, un teléfono, una laptop, etc.
- Internet: es toda la red formada por servidores y clientes que proveen y consumen contenidos web y se comunican entre sí a nivel global.
- Server (servidor): es un computador, ubicado en alguna parte de la red, que está prendido todo el tiempo, en el que se alojan o almacenan sitios web y sus recursos y al cual se accede a través de nombres de dominio (.com, .net, .pe, etc.). También se les conoce como hosting.

Profesiones dentro del Desarrollo Web:

- **Frontend**: son los encargados de cuidar toda la apariencia y experiencia de usuario. Su misión es pasar todo el diseño gráfico de un sitio o aplicación web, a código, y proveer toda la interactividad a los clientes. Esta rama se puede subdividir en algunas especializaciones como: Arquitecto Frontend, Desarrollador JavaScript (frontend), etc.
- **Backend**: resguardan los datos y la seguridad de las aplicaciones y sitios web. Su misión es crear y mantener toda la parte del sitio web que sucede en los servidores. Pueden especializarse aún más en: SysAdmis, DevOps, Desarrollador JavaScript (backend), entre otros.

Las tres tecnologías básicas que debe conocer y manejar un Frontend son:

- **HTML**: es el lenguaje de marcado para hacer websites.
- **CSS**: hojas de estilos cascada, el diseño hecho código.
- **JavaScript**: es el único lenguaje que funciona actualmente dentro de los navegadores de manera nativa."

## DOM

DOM es el acrónimo de Document Object Model o Modelo de documento, y es la manera en que se representa el contenido del documento, de manera similar a un árbol de nodos.

A continuación, un ejemplo sencillo de la estructura del DOM:

```
html
    head
        title
        meta
    body
        header
            nav
        section
            article
        footer
```

## Etiquetas

Las etiquetas son la representación básica de la información en un documento html. Sirven para crear y organizar el contenido.

`<nombre> contenido </nombre>`

*Para más información visitar* [html5doctor](https://html5doctor.com)

Algunas de las etiquetas más conocidas y usadas son:

- Etiquetas de cabecera (head)
    - **doctype**: indica al navegador el tipo de documento que se está mostrando.
    - **html**: es la etiqueta que envuelve todo el documento
    - **head**: es la cabecera del documento y contiene sub etiquetas que describen al documento o incluyen recursos adicionales.

- Etiquetas del cuerpo del documento (body):
    - **article**: diferencia partes del contenido que pueden vivir por sí mismas.
    - **nav**: para hacer menús de navegación.
    - **aside**: contenido menos relevante, como publicidad, etc.
    - **section**: sirve para diferenciar las secciones principales del contenido.
    - **header**: cabecera del documento.
    - **footer**: pie de página del documento.
    - **h1 - h6**: títulos de nuestro sitio web.
    - **table**: tablas de contenidos, similar a la estructura de las hojas de calculo.
    - **ul y ol**: listas de items.
    - **div**: cualquier división para organizar el contenido.

    ## Estructura de nuestro Sitio Web

El archivo **index.html** es el archivo que el navegador abre por defecto al acceder a un directorio en un servidor web.

La estructura básica de un archivo html es la siguiente:

```html
<html>
  <head>
    <title> Título de la página title>
  head>
  <body>
    <header> Cabecera del contenido header>
    <section> Sección principal section>
    <section> Otra sección section>
    <footer> Pié de página del documento footer>
  body>
</html>
```

## Continuando con la estructura de nuestro Sitio Web

La estructura html de nuestro proyecto usa una o más de las siguientes etiquetas:

- **h1 a h6**: son etiquetas para indicar títulos con un estilo que destaca del resto.
- **article**: es la parte de nuestro contenido que puede vivir por sí mismo. Pueden haber tantos artícle como proyectos o eventos tenga nuestro portafolio.
- **p**: define el texto de un párrafo.
- **small**: aplica una apariencia de texto reducido en tamaño.
- **strong: aplica al texto un formato de negritas.
- **a**: corresponde a un ancla o enlace a una url interna o externa del documento.
- **img**: con esta etiqueta podemos enlazar imágenes en el documento.
- **figure**: le da un contexto semántico a las imágenes.


## Atributos HTML

Los atributos son valores agregados a las etiquetas (tags) html que extienden su habilidad o funcionalidad con información específica.

A continuación, un ejemplo de los atributos más comunes y usados en algunas etiquetas:

Para **img**:

- **src**: específica la ruta de la imagen que será mostrada a través de esta etiqueta. La ruta puede ser absoluta (cunado especifica una dirección exacta, incluyendo el prefijo http(s) ) o relativa (cuando la referencia a la ubicación de la imagen parte de la ubicación del archivo actual).
- **alt**: indica un texto alternativo que será mostrado en lugar de la imagen cuando ésta no pueda ser mostrada.
- **width**: ancho de la imagen en pixeles.
- **height**: alto de la imagen en pixeles.

Para **link**, en la *cabecera* head del documento:

- **rel**: indica la relación del recurso con el contenido.
- **type**: indica el tipo de recurso / formato.
- **href**: indica la ubicación (url) del recurso enlazado.

Para **meta**, ambién en la cabecera head del documento:

- **charset**: indica la tabla de caracteres (utf-8 para caracteres latinos) usada en el documento.

Para **a**:

- **href**: la ubicación o ruta a la que enlaza esta etiqueta de ancla. En el caso de querer enlazar a elementos que se encuentran dentro del mismo documento, este atributo debe indicar el valor del atributo ““id”” de ese elemento destino del enlace.


## Formularios HTML

Los Formularios en html son unidades de información que nos permiten recolectar información para enviarlos al propietario del website o a un servicio externo. Esta formado por dos partes o contextos: una parte donde se hace el ingreso y modelación de esos datos (en el frontend), y otra parte que se encarga de enviar, procesar y almacenar esos datos (en el backend).

Los formularios se crean con la etiqueta **form**. El atributo principal de un formulario es *action*, ya que contiene la ruta a la que serán enviados los datos recolectados.


## Formas de agregar estilos a HTML

Hay tres opciones para incluir estilos que definan la apariencia de tu html:

- **Estilos en línea**: se definen directamente en el elemento html que quieres estilizar, se agregan con el atributo style.
- **Estilos con el tag Style**: regularmente este tag se incluye dentro de la etiqueta head del html.
- **Estilos enlazados desde un archivo css externo**: utilizando la etiqueta link que nos permite enlazar recursos externos.

A **CSS**, se le llama **hojas de estilos en cascada** porque los estilos que se definen para una página, se van aplicando de arriba hacia abajo, y de lo más general a lo más particular, teniendo prioridad lo más particular. Esto es, los estilos que prevalecen son los que han sido definidos en línea, luego los que fueron definidos mediante la etiqueta style en la cabeza o cuerpo del html, y por último los estilos definidos en archivos externos enlazados con la etiqueta **link**. Esta prioridad se puede alterar al usar el modificador **!important** en la definición de algún estilo en particular, aunque esto no es recomendado.


**Enlace importante para aprender CSS** https://flukeout.github.io/

## Los estilos incluidos por el navegador

Los navegadores incluyen estilos predeterminados para cada elemento html. Esto significa que aún cuando no hayas definido o asignado ningún estilo a tus etiquetas, éstas tendrán una apariencia particular que es muy similar en todos los navegadores, aunque no necesariamente idéntica.


## Agregando clases a los componentes escritos en HTML

Para aplicar estilos a los componentes html, lo más común y recomendable es hacerlo a través de clases que se asignan al elemento html mediante el atributo class.

Un elemento html puede tener varias clases, se deben indicar en el mismo atributo class pero separadas por un espacio en blanco.

Al escoger los nombres de clases, debemos tener en cuenta que se puedieran aplicar a muchos elementos, o a elementos particulares, así que la claridad y precisión en su identificación facilitará la contextualización y mantenibilidad en el futuro.

Algunos de los estándares más usados para la identificación de clases son:
- [OOCSS](https://www.keycdn.com/blog/oocss)
- [BEM](http://getbem.com/naming/)
- [Component CSS](https://www.sitepoint.com/introducing-ccss-component-css/)


