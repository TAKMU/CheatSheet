# JQuery
Documentación: 
https://api.jquery.com/
Modificar elementos html y crear elementos.  
Biblioteca de JS, simplicando elementos de html del DOM, gestionar eventos, manipular hojas de estilos CSS, crear efectos o animaciones, con AJAX, obtener elementos del servidor.

## Enlazar Jquery

Se puede ligar directamente de internet
```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
```
Se puede descargar y hacer host en el proyecto: 
```
npm install jquery
```
## Selectores y tipos
Se utiliza *$("selector")
* Básicos  

  **id**  
    *$("#id")*  
  **clase**   
    *$(".clase")*  
  **elemento, nombre de etiqueta**   
   *$("elemento")*  
    *$("p")*  
  **multiple**   
    *$("elemento, #laId, .laClase")*  
  
* Básicos con filtro
    \:first, primer elemento que coincida con el selector  
    \:last, ultimo elemento que coincida con el selector  
    \:not(), elemento que no coincida con el selector  
    
* Atributos
[atributos] todos los atributos que contengan el valor  
[\*atributos] todos los atributos que contengan la subcadena indicada  
[$]atributos especificos que contengan al final la subcadena indicada  
[!]elementos que no tengan el valor exacto. 
* Formularios  
\:text: apunta a todo texto del folmulario  
\:password: apunta a todos los elementos de tipo password.  
\:submit: apunta a todos los elementos de tipo submit.   
\:radio : apunta a todos los elementos de tipo radio.  
\:checkbox: apunta a todos los elementos de tipo checkbox.  
\:checked: apunta a todos los elementos checados (checkbox).  

## Objeto event
Se utiliza el objeto evento, para pasar el evento a unas funciones como parametro para ampliar el rango de métodos y propiedades.  
#().click(function(event){metodo y propiedades});  
Hay varias propiedades:  
* which: regresa el código de la tecla pulsada. 
* clientX: regresa las coordenadas del puntero en x (considerando la izquierda como 0)
* clientY: regresa las coordenadas del puntero en y (considerando la parte superior como 0)
Hay varios métodos:  
* preventDefault: evita que se ejecute una acción asociada al evento (evitar enviar la información del formulario atravéz del botón submit).
* preventPropagation: evita que se propague o se escuche la acción de un elemento a otro (padre-hijo).  

## Eventos y tipos

Pulsación del teclado, entre otros  
*$("selector").evento(function(){});*
* Ratón

click
dblclick
mousedown (pulsación de cualquier botón)
mouseup (cuando se deja de presionar el botón)
mouseenter, cuando entra en el elemento seleccionado.  
mouseover, cuando el ratón está dentro del elemento.  
mouseout, cuando el ratón sale del elemento seleccionado.  
mousemove, cuando el raton se está moviendo   
* Teclado  
keydown, la pulsación del teclado
keypress, cuando la tecla esta presionada
keyup, cuando se suelta una tecla

* Formulario


## Métodos y tipos
Función que realiza una acción: mostrar elementos, cambiar de elementos
*$("selector").metodo(parametros);*
* clase
addClass() Añade clase  
removeClass() Elimina clase  
toggleClass() Añade y elimina clases de manera alterna  
hasClass() Checa si tiene una clase  

* asignan u obtienen
text, obtiene o se asigna texto dentro de una etiqueta html. 
html, ingresa o recoje codigo html dentro de una atiqueta
val, obtuene el valor del atributo value del elemento
attr, asigna o se obtiene el atributo del elemento html seleccionado
removeAttr, remueve el atributo del elemento html seleccionado
* dentro
append: inserta al final, dentro del elemento seleccionado. 
preppend: inserta al inicio, dentro del elemento seleccionado. 
* antes o despues
after: después del elemento
before: antes del elemento 
* muestran u ocultan
hide: oculta elemento seleccionado.  
show: muestra elemento/elementos seleccionados.  
slideDown: muestras con elemento de deslizado.  
slideUp: ocultas con elemento de deslizamiento.  
slideToggle: muestras u ocultas elementos con efecto de deslizamiento.   
* CSS
* text: 
* formulario:
submit: detecta cuando se presiona el botón de formulario.   
select: cuando se selecciona un texto.  
focus: cuando un elemento toma el foco.   
blur: cuando un elemento pierde el foco  

**$(selector).css()**
```
<p style="color:red; font-size:16;">Método CSS </p>
var estilo= $(selector).css();
//estilo=={color:red; font-size:16}

```
$(selector).css("color", "red");
$(selector).css({"color": "red", "font-size": "14px"});

### ready
Modelo de objeto esté listo. Evita que se ejecuten funciones y fallen antes de que se cargue el documento DOM.

```
$document.ready(function(){}
$("button").click(function(){
  $("p").slideToggle();
  });
});
```

