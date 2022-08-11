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


## DOM (Document Object Model)
Metodos para obtener elementos

getElementByTagName
    document.getElementByTagName("nombre_etiqueta")[indice];
    document.getElementByTagName("div")[2];
    //tercer elemento div
    
getElementByName
    document.getElementByName("nombre_atributo");
    document.getElementByTagName("edad");
    
getElementById
    document.getElementById("atributo_id");
    document.getElementByTagName("principal");
