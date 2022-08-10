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
    
    
  ### Sub-objeto imagen
    
    
  ### Sub-objeto de formulario
    
  ### Sub-objeto de formulario
    document.title ="un_titulo"  
    
  ### Sub-objeto de write
    document.write("escribe en el documento");  
  </details>
</details>
