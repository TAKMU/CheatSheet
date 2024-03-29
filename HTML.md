### Estructura básica
<details> 
  
#### Esqueletos
<details>

```
<!DOCTYPE html>  
<html> 
 <head> 
 </head>
 <body>  
 </body>
</html>
```

</details>

#### Para acentos
<details>

  ```
<meta charset="utf-8">
```
</details>

#### Encabezados 
<details>

h(n), n tiene 6 niveles, y 1 es de mayor importancia
```
  <h1>...</h1>  
```
</details>

#### Párrafos y Saltos de linea 
<details>

Un párrafo
```
<p>...</p> 
<br/>
 ```
</details>

#### Contenedores
  <details>
  
##### div

    Nivel de bloque
##### span

    Nivel de linea
  </details>
  
  #### Formatos
<details>
  
  <details><summary>Negritas</summary>

```
  <b> Formatea el texto en negrita </b>
  <strong> Formatea el texto en negrita y TIENE IMPORTANCIA SEMANTICA </strong>
```
  </details>
  <details><summary>Cursiva</summary>
    
```
  <i> Formatea el texto en negrita y tiene importancia semántica </i>
  <em> Formatea en itálica o cursiva y tiene importancia semántica </em>
```
  </details>
</details>

  #### Atributos
  <details>
    
*  **width**: anchura

*  **height**: altura

*  **id**: identificador único al elemento o etiqueta que se le aplique.

*  **class**: identificador común a las etiquetas (plural), para aplicar estilos o interactividad
  </details>
  
  </details>
  
### Elementos
<details>
  
   #### Imagen
  <details>
    
 *No necesita etiqueta de cierre, necesita una ruta de la imagen, y se le puede agregar los atributos width y height*  
 
##### Atributos
    
<details>
      
  **width**, **height**, **src** (se explicaron en atributos y al inicio de seccion).  
      **alt**: Texto alternativo  
      **tittle**: Texto flotante al situarnos encima con el mouse  
      
</details>
    
    
 ```
 <img src=""/>
 <img src=""/ alt="No se puede mostrar la imagen" title="imagen de gatitos">
 ```
 
    
  </details>
  
  #### Enlace o link  
  <details>  
    
  Conexión a información o documento al pulsar a este.  
  Atributo esencial es **href** para indicar el destino.  
    Atributo **target** indica como se abre el link.  (*target = "_blank"*, para abrir en otra pagina; existen otros más como *"_self"* para abrirla en la misma sección . *"_parent*, *"_top*", o *"framename"* para un marco en específico).  
  ```
  <a href="www.prueba-allan.ddnsfree.com"> </a>
  <a target = "_blank" href="www.google.com"></a>
  ```
    
  </details>
  
  #### Listas
  <details>
    
##### Listas ordenadas

<details>

  Crear listas ordenadas.
      
```   
      <ol type="1">
        <li value="1">Empieza con 1. </li>
        <li>2.</li>
        <li>3.</li>
      </ol>
```
  
  ###### Atributos
  <details>
    
```
    <ol start="number"> Define numero inicial, default es 1 o toma el equivalente en su numeración (2=b)</ol>
    <ol type="A|a|1|I|i"> Define el tipo de numeración: alfabética, numeral, romano </ol>
    <li value="number"> Define valor equivalente al tipo de numeracion por elemento de lista</li>
```
    
  </details>

      
</details>
    
##### Listas desordenada
   
<details>
  
Unordered list es una lista sin prioridad u orden. Default es disk o circulo rellenado. 
```
  <ul>
    <li> </li>
  </ul>
```
*ATRIBUTOS*
<details>
  
  type="circle|square|disk|none"
</details>
  
</details>
    
##### Listas de definiciones
   
<details>
  
Definition list es lista para definiciones (parecido a un diccionario)
```
  <dl>
    <dt>Termino que definiremos </dt>
      <dd>1ra definicion    </dd>
      <dd>2a definicion    </dd>
    <dt>2o termino</dt>
      <dd></dd>
  </dl>
```

  
</details>
 
  </details>
  
#### Tablas
  
<details>

* tr=renglón
* td="columna o entrada, celda"
* th=encabezado, negritas
  
```
  <table>
    <tr>
      <th>Encabezado</th>
    </tr>
    <tr> 
      <td>"celda de columna", table data</td>
    </tr>
  </table>
```
**ATRIBUTOS**
<details>
  
  <table>
    <tr>
      <th>Etiqueta</th>
      <th>Atributo</th>
      <th>Definicion</th>
    </tr>
    <tr>
      <td rowspan="2"> td, tr </td>
      <td> colspan="number" </td>
      <td> Agrupar una celda con varias columnas </td>
    </tr>
    <tr>
      <td> rowspan="number" </td>
      <td> Agrupar una celda con varios renglones </td>
    </tr>
  </table>
</details>
</details>
  
#### Formularios
<details>
  
  Formularios para ingreso de datos de usuarios
```
  <form action="http://destino.com" method="POST"/>
    Nombre de Usuario: <input name="nombreUsuario" value="valor por defecto" type="text"><br> <!--texto-->
    Estas vivo: <input name="status" type="checkbox" checked="checked" value="selecionada"> <!--checked selecciona la casilla por default, al mandar información manda el contenido de value.--> <br>
    Quieres:<br>
    Comer <input name="acciones" type="radio" value="comer"><br>
    Dormir <input name="acciones" type="radio" value="dormir"><br>
    Jugar <input name="acciones" type="radio" value="jugar"><br>
    Password <input name="password" type="password">
    Secreto <input name="secretos" type="hidden" value="nuevoDatoOculto">
    Reset <input type="reset" value="restablecer o reiniciar">
    Enviar <input type="submit" value="enviar">
  </form>
```
  
  </details>
#### Otros tipos de entrada
<details>
#####  Listas desplegables

<details>
  
Lista desplegable

```
<select name="lista" size=1 multiple>
  <!-- multiple permite seleccionar más de uno, size es la cantidad de opciones que se muestran. -->
  <option value="Sistemas" >Programacion</option>
  <option value="Negocios" selected="selected">Administracion de empresas </option>
  <!-- Selected va a ser el valor de default -->
</select>
```  

</details>

##### Area de texto
<details>
  
```
  <textarea name="nombre del elemento" value="default" cols=34 rows=2>
    Numero de letras de ancho 34, y 2 lineas
  </textarea>
```
</details>
</details>

#### Navegación (links agrupados)
<details>
 Conjunto de ligas agrupadas.
```
  <nav>
    <ul>
      <li>Inicio</li>
      <li>Enlaces</li>
      <li>Descargas</li>
      <li>Sobre mi</li>
      <li>Contacto</li>
    </ul>
  </nav>
```
</details>
  </details>
