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