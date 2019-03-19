# Fonts
Las fuentes nos permiten agregarle una de las caracteristicas de la personalidad de nuestro diseño. Para agregar fuentes a travez de css. Se hace a travez de las especificaciones de font. 

## font-family
A travez de la declaracion __font-family__ podremos elegir el tipo de familia para nuestro elemento seleccionado.
```
p {
   font-family: 'arial';
}
```

## font-size
A travez de la declaracion __font-size__ podremos declarar el tamaño de nuestra fuente.
```
p {
   font-size: 12px;
}
```

## font-weight
A travez de la declaracion __font-weight__ podremos declarar el grosor de nuestra fuente.
```
p {
   font-weight: "bold";
}
```

## font-style
A travez de la declaracion __font-style__ podremos declarar el estilo de nuestra fuente, teniendo como valor mas usado __italic__.
```
p {
    font-style: "italic";
}
```

## line-height
A travez de la declaracion __line-height__ podemos manipular el interlineado de cada palabra en un texto.
```
p {
    line-height: 20px;
}
```

## text-align
A travez de la declaracion __text-align__ podemos manipular la posicion de un texto dentro de una caja. Tenemos los valores "left, center, right".
```
p {
    text-align: "left";
}
```

## Definicion Shorthand
A Travez de las definiciones shorthand podemos definir estilos mas cortos a travez de una sola etiqueta, en este caso la etiqueta __font__
```
p {
      font: font-style font-variant font-weight font-size/line-height font-family;
}

body {
  font: italic small-caps normal 13px/150% Arial, Helvetica, sans-serif;
}
```

Para usar shorthand como minimo se deber declarar el tamaño de fuente y la familia;
```
body {
  font: italic 20px Serif; /* works */
  font: 20px; /* fails */
  font: 18em Fantasy; /* works */
  font: bold small-caps; /* fails */
}
```



