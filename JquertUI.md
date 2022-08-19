# JQueryUI
Jquery user interface. Conjunto de elementos pluggins para interacciones de usuario. 
Documentación: https://api.jqueryui.com/  
Puedes descargar el archivo desde la página de jqueryui o colocar un link para el código directamente (indicando la versión de jquery). Además, en ciertos casos, se necesita la hoja de estilos de jquery-ui.  
En las descargas, puedes elegir sólo los elementos necesarios y ligar directamente los elementos. 
```
  <style>
      <link rel="stylesheet" href="//code.jquery.com/ui/1.13.2/themes/base/jquery-ui.css">
  </style>
  <script src="https://code.jquery.com/jquery-3.6.0.js"></script>
  <script src="https://code.jquery.com/ui/1.13.2/jquery-ui.js"></script>
```
Esta es la forma para descargar por medio de npm, tiene dependencia de jquery. 
```
npm install jquery
npm install jquery-ui
``` 
## Interacciones:
Para interacciones, necesita estar dentro de una función: 
```
  $( function() {
    $( "selector" ).interaction(options);
  } );
```
### Arrastrable
Utilizar el "método" draggable para que los elementos puedan ser modificados. 
```
  $( function() {
    $( "#draggable" ).draggable();
  } );
```
Opciones: 
* containment: Es una opción o parámetro para que se coloque el elemento, en el elemento padre, documento o ventana que lo contenga. 
```
  $( function() {
    $( "#draggable" ).draggable(containment: "parent|document|window");
  } );
```
* cursor: cambia la imagen del cursor al arrastrar. Puedes utilizar todas las opciones de CSS (https://www.w3schools.com/cssref/pr_class_cursor.asp).
```
$("selector").draggable(cursor: "move|pointer|...");
```
* delay: retrasar el arrastre de los elementos por milisegundos
```
$("selector").draggable(delay: tiempo);
```
* grid: mover en forma de cuadricula, que se mueva por x pixeles. 
```
$("selector").draggable(grid: [distancia x, distancia y]);
```
* helper: elemento auxiliar (clon) para arrastrar en vez del elemento original. 
```
$("selector").draggable(helper: "clone");
```
* zindex: para proporcionar un nivel de capa mientras se arrastra. 
```
$("selector").draggable(zindex: nivel de capa (num));
```
* stack: llevar el elemento a la capa más alta, indicar los elementos (selectores) que son apilables. 
```
$("selector").draggable(stack: ".selector");
```
* enable() y disable(): para habilitar o deshabilitar del elemento
```
$("selector").draggable("enable|disable");
```
* start: cuando se empieza arrastrar un elemento
* drag: mientras está arrastrando, utilizar una función. 
* stop: cuando se termine de arrastrar, utilizar una función. 
Se necesita separa con coma, en caso de que se utilicen más de un atributo. 
```
$("selector").draggable(
  start: function(){},
  drag: function(){},
  stop: function(){},
  );
```
### Soltable / droppable.  
Se utiliza para elementos que interactuan con elementos arrastrables
* drop: cuando soltamos un elemento arrastrable sobre un elemento soltable. 
* over: cuando un elemento arrastrable pase sobre un elemento soltable.
* out: cuando un elemento arrastrable sale de un elemento soltable. 
```
$("selector").droppable(
  drop: function(){},
  over: function(){},
  out: function(){}
);
```
* accept: para que acepte los elementos "draggable".
```
$("selector").droppable(
  accept: "#selector";
);
```
* tolerance: para ver la tolerancia para "aceptar" el draggable. fit es para que todo el arrastrable esté dentro del elemento, intersect es para que se considere cuando 50% esté dentro del elemento. 
```
$("selector").droppable(
  tolerance: "fit|intersect";
);
```
* enable y disable: habilitar y deshabilitar los elementos.
```
$("selector").droppable(
  "enable|disable"
);
```
### Sortable
Una lista en los que sus elementos se puede ordenar
```
$(function(){
  $("selector").sortable(
  );
});

```
* axis: para que solo se ordene por un axis x o y.
```
$(function(){
  $("selector").sortable(
    axis: "x|y"
  );
});

```
* cancel: que limitan a ciertos elementos no pueden estar ordenados. 
```
$(function(){
  $("selector").sortable(
    cancel: "selector, selectorb"
  );
});

```
* cursor: cambiar la imagen del cursor, los mismo de CSS (https://www.w3schools.com/cssref/pr_class_cursor.asp).
```
$(function(){
  $("selector").sortable(
    cursor: "move"
  );
});

```
* grid: Ordenar los elementos de cuadrícula. 
```
$(function(){
  $("selector").sortable(
    grid: [horizontal, vertical]
  );
});

```
* start, stop, update: para poner indicaciones cuando se empiece a ordenar, se termine y cuando se actualizan las posiciones. 
```
$(function(){
  $("selector").sortable(
    start: function(){},
    stop: function(){},
    update: function()
  );
});

```
### Resizable
Para que un elemento pueda ser redimensionado.
```
$(function(){
  $("selector").resizable(
  );
});
```
* animate, animateduration, animateeasing: para animaciones mientras se redimensiona.  animateEasing es para tipo de animacion. 
```
$(function(){
  $("selector").resizable(
    animate: true,
    animateduration: "fast|slow|milisegundos",
    animateEasing: "easeOutBounce"
  );
});
```
* aspectRatio: para que tenga cierta proporción de dimensiones
```
$(function(){
      $("selector").resizable( 
        aspectRatio: true
  );
});
```
* grid: agrandar o minimizar por cuadrícula
```
$(function(){
  $("selector").resizable(
    grid: [x, y]
  );
});
```
* animate, animateduration, animateeasing: para animaciones mientras se redimensiona.  animateEasing es para tipo de animacion. 
```
$(function(){
  $("selector").resizable(
    animate: true,
    animateduration: "fast|slow|milisegundos",
    animateEasing: "easeOutBounce"
  );
});
```
* ghost: creará un "clon" semitransparente
```
$(function(){
  $("selector").resizable(
    ghost: true
  );
});
```
* containment: contenedor que limita el elemento redimensionable por su elemento padre. 
```
$(function(){
  $("selector").resizable(
    containment: "parent"  
  );
});
```
* maxHeight, maxWidth: limita el ancho y alto de un elemento redimensionable. 
```
$(function(){
  $("selector").resizable(
    maxHeight: y, 
    maxWidth: x
  );
});
```
* minHeight, minWidth: limita el ancho y alto de un elemento redimensionable. 
```
$(function(){
  $("selector").resizable(
    minHeight: y, 
    minWidth: x
  );
});
```
* start, stop, resize: Es para dirigir el comportamiento mientras (resize), después (stop) y cuando empieza (start) a redimencionar.
```
$(function(){
  $("selector").resizable( 
    start: function(){},
    stop: function(){},
    resize: function(){}
  );
});
```
