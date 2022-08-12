# JavaScript
## Básico
<details>
  
## Incorporar JS
* Dentro de etiquetas.
* En etiquetas script
* En un documento aparte (script src="")
## Variables
Se inicia con *var* o *let*.
```
var hola="mundo";
let i=0;
```
</details>

## Array, métodos  
<details>
  
* push (elementos al final del array). Regresa todos los elementos
* unshift (elementos al principio del array). Regresa todos los elementos
* sort (ordena los elementos)
* shift (elimina el primer elemento de un array)
  
</details>


## Funciones
<details>

```  
function nombre(argumentos){
  proceso;
}  
```

</details>

## Objetos nativos
<details>
  
### window
  No es necesario nombrarlo. Por ejemplo, window.document.bgcolor es igual a document.bgcolor
  <details>
  
#### Alto y ancho interno de la ventana
    innerwidth, innerheight
    
#### Alerta de la ventana, entrada de datos
    alert(), prompt("descripcion");
    
### Abre nueva ventana y cierra ventana activa
    open("url, nombreVentana, specificaciones"), close()
    
    
### Ejecuta código por intervalos o ejecutar al pasar un tiempo
    
    setInterval(function(){}, tiempo por milisegundos), setTimeOut(function(){}, tiempo por milisegundos)
  </details>
  
### Document
Sub-objeto de windows, maneja propiedades y elementos principales del documento web. 
  <details>
  
#### Sub-objeto url
    document.url, url del documento
    documento.url="una_url"
    
#### Sub-objeto anclaje
    
    
#### Sub-objeto imagen
    
    
#### Sub-objeto de formulario
    document.title ="un_titulo"  
    
### Sub-objeto de write
    document.write("escribe en el documento");  
  </details>
  
### Date
No tiene propiedades pero tiene métodos
  <details>  
    
    Lectura: get para obtener, consultar el tiempo  
    Escritura: set para inicializar el objeto.  
    Conversión: convierten en string o milisegundos
  </details>
  
### String
Manipular las cadenas de texto, tiene solo la propiedad lenght y multiples métodos
  <details>  
    
    indexOf: posición de la ocurrencia
    lastIndexOf: ultima ocurrencia 
    subString: devuelve una subcadena
    replace: reemplaza con otra cadena. 
  </details>
  
### Screen
Solo propiedades
  <details>  
    
    width: anchura pantalla
    height: altura pantalla.
    availWidth: anchura de pantalla disponible para uso de ventanas
    availHeight: alturo de pantalla disponible para uso de ventanas
  </details>
  
### Navigation
Plataforma utilizada por el usuario (mozilla, chrome, entre otros)
  <details>  
    
    platform: plataforma se está ejecutando el navegador
    appName: nombre del navegador
    appVersion: la versión del navegador
    
    Metodo 
    javaEnable: Si la plataforma está habilitada para poder ejecutar el código JS
  </details>
  
### Location
Partes que forman una URL
  <details>  
    
    href: url completa
    hostname: nombre del dominio del servidor dentro del url
    protocol: protocolo de la pagina web
    
    Metodo 
    reload: Carga de nuevo la página.
    replace: cambia el url por otro
  </details>
  
</details>

## DOM (Document Object Model)
Modelos de objetos del documento. Estructura de objetos que genera el navegador, se puede modificar con JS o jQuery. Abarca desde el navegador hasta los documentos (también etiquetas de html). Acceso directo a una página web. 


## Obtener elementos de la pagina web
<details>

Metodos para obtener elementos  

getElementByTagName  
```
    document.getElementByTagName("nombre_etiqueta")[indice];
    document.getElementByTagName("div")[2];
    //tercer elemento div  
```
   
getElementByName 
```
    document.getElementByName("nombre_atributo");
    document.getElementByTagName("edad");
```
    
firstElementChild
```
  <ul id="lista">
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
    var lista=document.getElementById("lista");
    lista.firstElementChild;
```
lastElementChild  
```
  <ul id="lista">
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
    var lista=document.getElementById("lista");
    lista.lastElementChild;
```
</details>

## Crear elementos de la pagina web
<details>

Metodos para crear elementos  

createElement 
```
    document.createElement("nombre_etiqueta");
    var div= document.createElement("div");
```
    
createTextNode
```
    document.createTextNode("texto_plano");
    var texto= document.createTextNode("creando elementos");
```

appendChild  
```
    var div= document.createElement("div");
    var texto= document.createTextNode("creando elementos");
    div.appendChild(texto);
    document.body.appendChilrd(div);
```
</details>

## Eliminar elementos de la pagina web
<details>

Metodos para eliminar elementos  

removeChild
```
  <div id="unico"></div>
  var div= document.getbyElementId("unico");
  document.body.removeChild(div);

```
</details>

## Obtener elemento padre de la pagina web
<details>

Metodos para obtener elemento padre, para evitar realizar ciclos para buscar el elemento y eliminarlo con removeChild

parentNode
```
  <div id="unico"></div>
  var div= document.getbyElementId("unico");
  div.parentNode.removeChild(div);

```
</details>

## Eventos
### Ratón
<details>
  
* onclick (boton izquierdo)
* ondbclick (doble boton izquierdo)
  
```
  <div onclick/ondbclick="unafuncion()"></div>
```
* onmousedown (mientras se presiona cualquier boton de mouse)
* onmouseup (si se retira el boton del mouse)
  
```
  <div onmousedown/onmouseup="unafuncion()"></div>
```
* onmouseout (mientras sale del elemento, mouse)
* onmouseover (si se pone el apuntador en el elemento)
  
```
  <div onmouseout/onmouseover="unafuncion()"></div>
```
</details>

### Teclado
<details>
  
* onkeydown (Si la tecla se presioan)
* onkeypress (mientras la tecla esté presionada)
* onkeyup (si deja de presionarse la tecla)
  
```
  <div onkeydown/onkeypress/onkeyup="unafuncion()"></div>
```

</details>

### HTML
<details>
  
* onkeydown (Si la tecla se presioan)
* onkeypress (mientras la tecla esté presionada)
* onkeyup (si deja de presionarse la tecla)
  
```
  <div onkeydown/onkeypress/onkeyup="unafuncion()"></div>
```
* onload: cuando el documento haya cargado totalmente
* onselect: cuando un trozo de texto es seleccionado.
* onchange: se pierde el foco cuando el texto sea modificado. 
* on submit: presionar el boton para enviar un formulario
* on resize: se redimensiona la pantalla del navegador
* onfocus: cuando estás enfocando a una entrada. 

```
 object.onfocus = function(){myScript}; 
  //or
  <input type="text" id="fname" onfocus="myFunction()">
  <script>
    function myFunction() {
      document.getElementById("fname").style.backgroundColor = "red";
    }
  </script>
}
```
</details>
