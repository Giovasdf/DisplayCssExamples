
# Distintos Valores de Display en CSS

## Introducción
Este documento está diseñado para ayudarte a comprender las diferencias entre varios valores de la propiedad `display` en CSS y cómo usar `flexbox` para organizar y alinear elementos dentro de un contenedor. Aprenderás sobre `block`, `inline`, `inline-block`, y `flex`, así como las propiedades asociadas con `flexbox` como `flex-direction`, `justify-content`, `align-items`, y `flex-wrap`.

## Estructura del Proyecto
El proyecto contiene un archivo HTML y CSS que ilustra los conceptos mencionados. A continuación, se explican las secciones clave del código.

## HTML

### Estructura Básica
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diferencias entre distintos valores de display en CSS</title>
    <style>
        /* Estilos CSS aquí */
    </style>
</head>
<body>
    <h1>Diferencias entre distintos valores de display en CSS</h1>
    <!-- Secciones de ejemplo aquí -->
</body>
</html>
```

### Secciones de Ejemplo

#### Display Block
```html
<h2>display: block</h2>
<p>Los elementos con display: block ocupan todo el ancho disponible de su contenedor y comienzan en una nueva línea.</p>
<div class="container block">
    <div class="box">Block 1</div>
    <div class="box">Block 2</div>
</div>
```

#### Display Inline
```html
<h2>display: inline</h2>
<p>Los elementos con display: inline no inician en una nueva línea y solo ocupan el espacio necesario para su contenido.</p>
<div class="container">
    <span class="box inline">Inline 1</span>
    <span class="box inline">Inline 2</span>
</div>
```

#### Display Inline-Block
```html
<h2>display: inline-block</h2>
<p>Los elementos con display: inline-block no inician en una nueva línea, pero permiten definir su tamaño con width y height.</p>
<div class="container">
    <span class="box inline-block">Inline-Block 1</span>
    <span class="box inline-block">Inline-Block 2</span>
</div>
```

#### Display Flex
```html
<h2>display: flex</h2>
<p>Los elementos con display: flex se organizan en un contenedor flexible. Puedes controlar la dirección, el alineamiento y la distribución de los elementos hijos.</p>

```
## Ejemplos de Flexbox

#### Flex Direction
```html
<h3>flex-direction</h3>
<p>La propiedad <code>flex-direction</code> define la dirección en la que los elementos flexibles se colocan en el contenedor.</p>
<div class="container flex-container flex-row">
    <div class="box">Flex 1</div>
    <div class="box">Flex 2</div>
    <div class="box">Flex 3</div>
</div>
```
#### Justify Content
```html
<h3>justify-content</h3>
<p>La propiedad <code>justify-content</code> alinea los elementos hijos a lo largo del eje principal (horizontal por defecto) del contenedor flexible.</p>

<h4>Center (centrar)</h4>
<div class="container flex-container flex-row justify-center">
    <div class="box">Flex 1</div>
    <div class="box">Flex 2</div>
    <div class="box">Flex 3</div>
</div>

<h4>Space Between (espacio entre)</h4>
<div class="container flex-container flex-row justify-space-between">
    <div class="box">Flex 1</div>
    <div class="box">Flex 2</div>
    <div class="box">Flex 3</div>
</div>

<h4>Space Around (espacio alrededor)</h4>
<div class="container flex-container flex-row justify-space-around">
    <div class="box">Flex 1</div>
    <div class="box">Flex 2</div>
    <div class="box">Flex 3</div>
</div>
```

#### Align Items
```html
<h3>align-items</h3>
<p>La propiedad <code>align-items</code> alinea los elementos hijos a lo largo del eje secundario (vertical por defecto) del contenedor flexible.</p>

<h4>Flex Start (inicio)</h4>
<div class="container flex-container flex-row align-start">
    <div class="box">Flex 1</div>
    <div class="box">Flex 2</div>
    <div class="box">Flex 3</div>
</div>

<h4>Flex End (final)</h4>
<div class="container flex-container flex-row align-end">
    <div class="box">Flex 1</div>
    <div class="box">Flex 2</div>
    <div class="box">Flex 3</div>
</div>
```

#### Flex Wrap
```html
<h3>Flex Wrap (ajuste)</h3>
<p>La propiedad <code>flex-wrap</code> permite que los elementos flexibles pasen a una nueva línea si no caben en una sola fila.</p>
<div class="container flex-container flex-row flex-wrap">
    <div class="box">Flex 1</div>
    <div class="box">Flex 2</div>
    <div class="box">Flex 3</div>
    <div class="box">Flex 4</div>
    <div class="box">Flex 5</div>
</div>
```

## CSS

### Estilos Generales
```css
.container {
    margin-bottom: 20px;
    border: 1px solid #000; /* Borde para visualizar el tamaño del contenedor */
    padding: 10px;
}
.box {
    width: 100px;
    height: 100px;
    background-color: #4CAF50;
    margin: 10px;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
}
.block {
    display: block;
}
.inline {
    display: inline;
    width: auto;
    height: auto;
}
.inline-block {
    display: inline-block;
}
.flex-container {
    display: flex;
    border: 1px solid #ccc;
    padding: 10px;
}
.flex-row {
    flex-direction: row;
}
.flex-column {
    flex-direction: column;
}
.flex-wrap {
    flex-wrap: wrap;
}
.justify-center {
    justify-content: center;
}
.justify-space-between {
    justify-content: space-between;
}
.justify-space-around {
    justify-content: space-around;
}
.align-start {
    height: 400px;
    align-items: flex-start;
}
.align-end {
    align-items: flex-end;
    height: 400px;
}
```

