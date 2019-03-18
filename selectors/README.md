#Selectores
Que son los selectores?. Bueno se habran preguntado como referenciamos los estilos a nuestro html. Asi es, a travez de los selectores podemos capturar un elemento de nuestro html y agregarle estilos. A continuacion veremos todas las formas.

## La mas basica es referenciar al nombre de la etiqueta.
```
p {
    /* aca escribimos nuestra declaracion css*/
}
```
como pueden observar se capturo el elemento html a travez del nombre de la etiqueta. Este enfoque es correcto cuando queremos declarar estilos de manera global, a travez de esta seleccion se le aplicaran los estilos a todos los elementos del tipo p.

## Descendentes.
```
p a {
    /* aca escribimos nuestra declaracion css*/
}
```
Tambien podemos seleccionar elementos dentro de otros. Como vemos en el ejemplo de arriba. A todas las etiquetas __a__ dentro de una etiqueta __p__. No existe un limite para realizar capturas descendentes pero lo ideal es no abusar de este tipo de capturas y tener como un maximo de una profundidad de hasta 4 descendentes.
```
//index.html
<body>
    <div>
        <ul>
            <li><a>link</a</li>
        </ul>
    </div>
</body>
```
En este codigo de arriba veamos la siguiente seleccion.
```
//index.css
div ul li a {
    /* aca escribimos nuestra declaracion css*/
}
```
Como pueden observar se ha hecho una declaracion descendente de una profundidad de hasta 4 selecciones. como maximo lo ideal es que nuestras declaraciones no superen esta cantidad; Por el motivo de que cuando querramos sobre escribir esta seleccion tendremos que hacer una seleccion mucho mas detallada para poder sobre escribirlo. y la cantidad de nuestro codigo crecera.


## Referenciando una clase.
```
//file.css
.clase {
    /* aca escribimos nuestra declaracion css*/
}
```
Que es una clase? Una clase es el nombre que declaramos explicitamente a un elemento html. Imaginemonos que solo queremos agregar estilos a una parte de nuestro diseño, no queremos capturar todos los elemtos de manera general. En estos casos bautizamos las etiquetas html con clases personalizadas. veamos el siguiente ejemplo.
```
//index.html
<body>
    <div class="bloque">
    </div>
</body>
```
En el codigo de arriba vemos el html con la clase llamada bloque. 
```
//index.css
.bloque {
     /* aca escribimos nuestra declaracion css*/
}
```
y como pueden observar en el codigo index.css, hacemos referencia a esta etiqueta y lo que escribamos dentro solo afectara a los elementos que tengan esta clase declarada.


## Referenciando por id.
Tambien podemos hacer referencias a travez de __id__. Este tipo de referencias no son recomendadas, ya que por pagina solamente se puede utilizar un id y los id se usan mas que todo para manejar logica js.
Para referenciar estilos id es de la siguiente manera.
```
#nombre_id {
     /* aca escribimos nuestra declaracion css*/
}
```

## Combinando selectores.
Hemos aprendido a hacer selecciones por etiqueta, por clase, por id. Tambien podemos hacer combinacion de todas estas. basta con que cumplan el orden de la descendencia y podremos atrapar a nuestro html. __Veamos algunos ejemplos__

```
#nombre_id .nombre-clase p {
     /* aca escribimos nuestra declaracion css*/
}
```
Como pueden observar hemos hecho una combinacion de selectores; todo dependera como declaremos nuestro arbol html; y en base a este orden de nuestro html haremos las selecciones.
```
.nombre-clase #nombre_id p {
     /* aca escribimos nuestra declaracion css*/
}
```

## Selectores Avanzados
Como parte de selectores avanzados veremos los siguientes.

## Selector de hijos
Este tipo de selector, solo seleccionara a los hijos directos. se indica mediante el signo __>__

```
index.css
p > span { color: blue; }
```
```
index.html
<p><span>Texto1</span></p>
<p><a href="#"><span>Texto2</span></a></p>
```

En el codigo de arriba podran observar que el elemento span es un hijo directo de la etiqueta p. Este afectara solamente al hijo directo.

## Selector Adyacente
Un selector adyacente solo afecta a 2 etiquetas que se encuentren una a la otra.
La seleccion se usa utilizando la etiqueta __+__

```
index.css
h1 + h2 { color: blue; }
```
```
index.html
<body>
<h1>Titulo1</h1>
<h2>Subtítulo</h2>

<h2>Otro subtítulo</h2>

</body>
```
En el ejemplo de arriba, veremos que solo la seleccion afectara al h1 y h2 que se encuentran juntos.

## Selector de atributos
Podemos realizar selecciones a travez de los atributos del html de la siguiente manera.
```
/* Se muestran de color azul todos los enlaces que tengan
   un atributo "class" con el valor "azul" */
a[class="azul"] { color: blue; }
```

## Selector de pseudoclases 
Los selectores de pseudo clase es un selector que añade un esta especial al elemento, 
los selectores mas usados son 
* __:hover__
* __:first-child__
* __:last-child__
* __:nth-child(n)__

## Enlaces de interes y de lectura obligatoria
* [selectores](https://developer.mozilla.org/es/docs/Web/CSS/Selectores_CSS)
* [selectores](https://alligator.io/css/css-selectors/)
* [pseudoclases](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes)
