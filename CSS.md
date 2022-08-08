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
<details>
  
**HTML**
```
  <h1>Prueba</h1>
  <div>
    <p>Se va a modificar esta sección</p>
    <span></span>
    <table></table>
  </div>
```
**CSS**
```
div, p, span, table{
...
}
```
</details>

* **Selectores de id y class**  
Apuntan a etiquetas con identificadores (id, class) de html. 

<details>

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
</details>

* **Selectores de atributos**
Apuntan a etiquetas con ciertos atributos o valores de los atributos. 
<details>

**HTML**
```
<a title="titulo">

<img title="flor sd">

<img title="flor gam">

<img title="hola-1">

<img title="hola-2">

<img title="holatres">

<img title="primeravez">

<img title="segundavez">

<img title="otravez">
```
**CSS**
```
#mild{
a[title]{
//Apunta al atributo title de la etiqueta a.

[title="titulo"]{
//valor de su atributo es titulo.
}

a[title="titulo"]{
//valor de su atributo es titulo y tiene la etiqueta a.
}

[title~="flor"]{
//Selecciona las etiquetas que contienen flor como palabra
} 
[title|="hola"]{
//Toma hola-1 hola-2, holatres no lo toma, porque no considera la palabra.
//Primera palabra
}
[title^="hola"]{
//Toma hola-1, hola-2 y holatres 
//Primera valor específico
}
[title$="vez"]{
//Toma hola-1, hola-2 y holatres 
//Terminen con un valor específico, todos los que terminan en vez.
}
[title*="ol"]{
//Toma hola-1, hola-2 y holatres 
//Contienen el valor en específico, no una palabra.
}
```
  
</details>

* **Selectores jerárquicos**
Apuntan a elementos HTML con jerarquía: descendientes, hijo, hermano adyacente y general de hermano (como tablas: tr y td(descendientes), td hijo de td,  
hermano adyacente tr y tr, entre otros.
  
  <details>

#### Descendientes
<details>
  
Toma a los elementos que se encuentren dentro de la etiqueta.  
  **HTML**
```
<div>
  <div><p></p></div>
  <span><p></p><p></p></span>
 <div>
   <p>Este no</p>
```
**CSS**
```
div p{
   //toma los elementos p que tienen un div como antecesor
   }
```
</details>
  
#### Hijos
<details>
  
Toma a los elementos que prosiguen inmediatamente del padre 
  **HTML**
```
<div>
  <div><p>Solo este elemento</p></div>
  <span><p>No</p><p>NO</p></span>
 <div>
   <p>Este no</p>
```
**CSS**
```
div > p{
   //toma los elementos p que tienen un div como padre
   }
```
</details>

#### Hermano adyacente
  <details>
  
Toma a los elementos que están de manera inmediata a su hermano 
  **HTML**
```
<div>
  <div><p>NO</p></div>
  <span><p>No</p><p>NO</p></span>
 <div>
 <p>Este SI </p>
 <p>Este no</p>
```
**CSS**
```
div + p{
   //toma los elementos p que tienen antes un div. 
   }
```
</details>
  
#### Hermano (general)
  <details>
  
Toma a los elementos que están al mismo nivel
  **HTML**
```
<div>
  <div><p>Solo este elemento</p></div>
  <span><p>No</p><p>NO</p></span>
 <div>
 <p>Este si</p>
```
**CSS**
```
div ~ p{
   //toma los elementos p que tienen antes un div. 
   }
```
</details>
   </details>



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
