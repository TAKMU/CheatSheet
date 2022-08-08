## CSS
### Maneras de insertar estilos:
* Estilo en línea:

```
<div style="codigo CSS">
```
* Hoja de estilo interna (cabecera o head):

```
<style> </style>
```
* Hoja de estilo externa:

```
<link rel="stylesheet" type="text/css" href="URL">
```
### Selector
Selector, conjunto de reglas utilizadas para apuntar a uno o varios elementos de un documento HTML  
* **Selectores de elementos**
Apuntan a etiquetas HTML, apuntan a etiquetas en CSS, el mismo nombre de la etiqueta (p, li, div, h1, table...)
* **Selectores de id y class**  
Apuntan a etiquetas con identificadores (id, class) de html.   

**HTML**
```
<div id="mild"></div> 
<div class="miClass"></div>
```
**CSS**
```
#mild{
atributo1: valor;
atributo2: valor;
}

.miClass{
atributo1: valor;
atributo2: valor;
}
```
* Selectores de atributos
* Selectores jerárquicos: Elementos hermanos, hijos, entre otros (tabla, tr, td)

*Se puede agrupar selectores de la siguiente manera*
```
div, p, span, table{
...
}
```

### Sintaxis

```
selector {
propiedad: valor;
propiedad2: valor;
}
```
### Modelo de caja
Margen, borde relleno, contenido

#### Padding
Margen interior (Por manecillas de reloj, empezando del superior)
```
<div id="cajita"></div>
<style>
  #cajita{
  padding: 10px 5px 10px 5px;
  }
  /*Iguales en funcion*/
  .gik{
  padding-top: 10px;
  padding-right: 5px;
  padding-bottom: 10px;
  padding-left: 5px;
  }
</style>
```
#### Margin
Margen exterior al elemento con relleno.
```
<div id="cajita"></div>
<style>
  #cajita{
  margin: 10px 5px 10px 5px;
  }
  /*Iguales en funcion*/
  .gik{
  margin-top: 10px;
  margin-right: 5px;
  margin-bottom: 10px;
  margin-left: 5px;
  }
</style>
```
#### Border
Definen estilo, grosor, color y redondeo del borde.
```
<div id="cajita"></div>
<style>
  #cajita{
  //
  border-style: dotted;
  //puntos
  border-style: dashed;
  //punteado (lineas)
  border-style: rished;
  //3D estriado
  border-style: inset;
  //efecto botón 3D
  border-style: solid;
  //continuo
  border-style: outset;
  //efecto botón 3D
  border-style: double;
  //doble linea
  border-style: hidden;
  //oculto
  border-style: groove;
  //3D acanalado
  border-style: none;
  //sin borde
  //puede colocar diferentes estilos por lado, igual como margen arriba y manecillas de reloj
  border-width: 2px;
  //puede colocar el ancho del borde al mismo tiempo.
  border-color: red;
  //puede colocar el color del borde al mismo tiempo.
  border-radius: 10px;
  //redondeo del borde, se puede hacer el borde al mismo tiempo, empezando de campo superior derecho. 
  border: 10px solid red;
  /*Especifica todos los puntos grosor, estilo y color*/
  }
  /*Iguales en funcion*/
  .gik{
  margin-top: 10px;
  margin-right: 5px;
  margin-bottom: 10px;
  margin-left: 5px;
  }
</style>
```
