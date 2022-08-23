# VueJS
https://vuejs.org/
Es un framework de Javascript para crear interfaces de usuarios. Incorpora HTML, CSS y JS. Puede colocarse en un solo documento: script (JS), style (CSS) y template (HTML). Arquitectura en componentes: data, components, methods.  
Se instala por parte de node.js de la siguiente manera:
```
npm install -g @vue/cli
vue create my-app
```
Donde my-app, es la carpeta de la aplicacion. Se entra a la carpeta y se ejecuta el comando npm run-serve para ejecutar el programa. 
```
cd my-app
npm run serve
```
Y se utiliza los siguientes comandos para acceder por Visual Studio Code.
```
cd my-app
code .
```
## Vue2
Se adjunta el código de la siguiente manera: 
```
<!-- development version, includes helpful console warnings -->
<script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
<!-- production version, optimized for size and speed -->
<script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
```
La sintaxis del código es la siguiente: 
CSS
```
<div id="app">
  {{ message }}
</div>
```
JS
```
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```
*Nota: No se puede instanciar un vue para la etiqueta html o body*
se hace una instancia de vue por cada elemento, y tiene ciertos elementos:
* **el:**  
Propiedad que elige el selector (css)
* **data:**  
Propiedad en donde se guardan los datos que se utilizarán en el elemento, instancia.  
Se guardan los datos de la siguiente manera:
  * **string**: 'string'
  * **boleano**: true|false
  * **array**: []
  * **objeto**: {nombreAtributo: valor, nombreAtributo2: valor}
 
* **{{$variable}}**  
Se reemplaza el valor sea por el valor de la variable o el resultado de una función. 
### Métodos
Reacciona a los eventos, se puede representar los eventos como v-on o como @. También se puede mezclar los métodos con Jquery.  
html
```
<p v-on:click="nuevoMensaje">{{mensaje}}</p>
/*o
<p @click="nuevoMensaje">{{mensaje}}</p>
*/
```
JS
```
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }, 
  methods: {
    nuevoMensaje: function(){
      this.mensaje = 'Perfecto! ya ves que es muy fácil.';
    }
  }
})
```
### Directivas
<details>
  
#### v-model
v-model se une los valores de un formulario o input. Asociando valores a la clabe de manera reactiva. 
<input v-model="mensaje" class="prueba">
JS
```
var app = new Vue({
  el: '#app',
  data: {
    message: 'Cambia el mensaje';
  }
})
```
#### v-show
v-show permite mostrar u ocultar el elemento en el que se encuentra. 
```
<main>
<div @click="ok=!ok"> Pulsa para alternar </div>
<div v-look="ok" class="animated bounceInLeft"> Ahora soy visible</div>
```
#### v-if
v-if elimina la etiqueta en la que se encuentra.
```
<div v-if="mensaje" class="animated rollIn"> La condición se cumple</div>
```
#### v-else
v-else necesita de v-if, para poder utilizarse. Funciona como else. 
```
<div v-if="mensaje" class="animated rollIn"> La condición se cumple</div>
<div v-else class="animated rollIn"> La condición no se cumple</div>
```
#### v-else-if
v-else necesita de v-if, para poder utilizarse. Funciona como elseif. Nueva opción. 
```
<div v-if="mensaje === 'A'" class="animated rollIn"> La letra es A</div>
<div v-elseif="mensaje === 'B'" class="animated rollIn"> La letra es B</div>
<div v-else class="animated rollIn">No es A ni B</div>
```
#### v-for
v-for es para iterar, realizar un ciclo. Este caso es para arreglos.
```
  <ul>
  <li v-for="ciudad in ciudades" class="animated rollIn"> {{ciudad.nombre}}</li>
  </ul>
```
Para objetos es:
```
  <ul>
  <li v-for="dato in datosUsuarios" class="animated rollIn"> {{dato}}</li>
  </ul>
```
Para mostrar la llave y el valor
```
  <ul>
    <li v-for="(value, key) in datosUsuarios" class="animated rollIn"> <b>{{key}}:</b> {{value}}</li>
  </ul>
```
#### v-text y v-html
Ingresará el valor del argumento dentro de la etiqueta. La diferencia, es que en html, se puede incorporar etiquetas html. 
```
  <div v-text="mensaje1"></div>
  <div v-html="mensaje2"></div>
```
#### v-bind
Asociar un atributo o etiqueta html con una expresión. Puedes cambiar de clase como en la línea 3 (considerando que tienes un estilo anterior. 
```
  <div v-bind:title="mensaje"> Colocate encima para mostrar su titulo </div>
  <div :title="mensaje">Es lo mismo, pero simplificado </div>
  <div :class="{rojo:claseRojo, borde:nuevoBorde} @click="claseRojo=!claseRojo"></div>
```
</details>

###Componentes
Los componentes son pedazos de código encapsulado con su propia lógica.
```
```
                                                                               ```
## Vue3
