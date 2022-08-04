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
