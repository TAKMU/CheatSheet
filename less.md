## LESS
Documentación  
https://lesscss.org/  
Less, preprocesador de CSS. El código less se utiliza un compilador y lo convierte a CSS.  
Se utiliza variables. Less utiliza menos líneas para más.  

### Variables
Se utiliza con @variable : valor;

<details>
  
**LESS**

```

@color: #333333;

body{
background-color:@color;
}
```
**CSS**

```

body{
background-color:#333333;
}
```
  
</details>

### Mixins  
Anidar dentro de otros estilos

<details>

**LESS**

```
.estandar{
    float: left;
    width: 200px;
    height: 200px;
    background-color: #FFFFFF;
    border: 1px solid #000000;
    border-radius: 10px;
}
  
#caja3{
    .estandar;
    box-shadow: @sombra; 
}
```
</details>

Recibir parámetros:

<details>

**LESS**

```
.caja(@ancho: auto, @alto: auto, @flota: left, @color: none, @desbordamiento: hidden){
    width: @ancho;
    height: @alto;
    float: @flota;
    background-color: @color; 
    -webkit-overflow: @desbordamiento;
    -moz-overflow: @desbordamiento;
    -ms-overflow: @desbordamiento;
    -o-overflow: @desbordamiento;
    overflow: @desbordamiento;
}
.borde(@grosor: 1px, @estilo: solid, @color: #111, @rad: 0px){
    border: @grosor @estilo @color;
    -webkit-border-radius: @rad;
    -moz-border-radius: @rad;
    -ms-border-radius: @rad;
    -o-border-radius: @rad;
    border-radius: @rad;

}
.sombra(@sombra: 5px 5px 5px #AAAA){
    -webkit-box-shadow: @sombra;
    -moz-box-shadow: @sombra;
    -ms-box-shadow: @sombra;
    -o-box-shadow: @sombra;
    box-shadow: @sombra;

}

#caja4{
    .caja(250px, 250px, right, @verde, hidden);
    .borde(2px, solid, #111AAA, 50px);
    .sombra(-25px 25px 25px #AAAAAA);
}
```
</details>

### Funciones de less
Cambiar de color, funciones matemáticas ya definidas. Puedes restar, sumar, multiplicar y dividir colores, anchos y largos, entre otros. 

<details>
  
```

  #caja1{
    float: left;
    width: 200px + 100px;
    height: 200px - 100px;
    background-color: #FF0000*2;
    border: 1px solid #000000;
    border-radius: 10px;
    box-shadow: 5px 5px 5px #AAAAAA;
}

#caja2{
    float: left;
    width: 200px;
    height: 200px;
    background-color: @azul - #555555;
    border: @grosor solid @negro;
    border-radius: @radio;
    box-shadow: @sombra; 

}
```
</details>

### Estilos anidados
Puede generar estilos anidados, uno dentro de otro
<details>

```
ul{
    .caja(250px, 250px, left, #FFF, hidden);
    .borde(2px, solid, #111AAA, 50px);
    .sombra(-25px 25px 25px #AAAAAA);
    margin: 10px;
    li{
        font-size: 20px;
        font-weight: 600;
        margin: 10px;
    }
}

```
  
  
### Alcance
Primero revisa las variables locales, y luego revisa si las variables existen en jerarquías más altas. 
<details>

```
@var: red;
  ul{
    @var: white;
    li{
        color: @var;
    }
}

```

En este caso toma el color blanco.
  
  ```
@var: red;
  ul{
    li{
        color: @var;
    }
    @var: white;
}

```
  
  Sigue tomando el color blanco.
  
</details>
