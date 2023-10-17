# Desafío CSS

## Objetivo:

- Crear un fondo con un patrón de rayas, cada raya de un color diferente.
- Cada `<div>` dentro del contenedor debe mostrarse como un círculo.
- Los círculos deben estar en una trayectoria diagonal a través del fondo de rayas.
- Debe haber un efecto de transición suave cuando pases el cursor sobre cada círculo, cambiando su color y tamaño.

## HTML:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Desafío CSS</title>
</head>
<body>
    <div class="container">
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
    </div>
</body>
</html>
```

## CSS (styles.css):

```css
.container {
    background: repeating-linear-gradient(45deg, #6414aa, #720b82 10px, #b82e04 10px, #b94f09 20px);
}
/* .container: aqui utilizo background que son lineas de colores que estan en el fondo del contenedor. Cada color se representará como una raya en el patrón. */

.circle {
    border-radius: 50%; /* .circle aqui puse border-radius para hacer que los <div> se muestren como circulitos miamsi de piu */
/* aqui hice que se posicionaran los círculos en una trayectoria diagonal */
    position: absolute;
/* y aqui puse la propiedad transition para lograr un efecto de transicion suave al pasar el cursor sobre cada circulo */
    transition: transform 0.3s ease-in-out, background-color 0.3s ease-in-out;
}

.circle:nth-child(1) {
    top: 10px;
    left: 10px;
}

.circle:nth-child(2) {
    top: 30px;
    left: 30px;
}

.circle:nth-child(3) {
    top: 50px;
    left: 50px;
}

.circle:nth-child(4) {
    top: 70px;
    left: 70px;
}

.circle:nth-child(5) {
    top: 90px;
    left: 90px;
}

.circle:hover {
    transform: scale(1.2);
    background-color: #a11ea1b6;
}
```

## Reglas:

- No se permite agregar o eliminar ningún elemento HTML.
- Solo edita el archivo CSS.
- No uses JavaScript ni ninguna librería de JS.
- Intenta completar el objetivo con la menor cantidad de código CSS posible.
- Está bien si no es perfecto al pixel, pero intenta hacerlo lo más cercano
