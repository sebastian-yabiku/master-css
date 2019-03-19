# Colors 
Para poder declarar colores tenemos 3 maneras de hacerlo, a travez de los valores __hexadecimales__, __rgba__ y __hsl__. Para definir colores tenemos las propiedades; __color__, __background-color__ y __background__.

# Hexadecimal
Los valores hexadecimales, son valores que se anteponen de una almohadilla y seguido de un numero de 6 caracteres.
```
p {
   color: #ffffff;
}
```

# rgba
La definicion rgba es un valor de 4 digitos, estos son __r=red, g=green, b=black, a=alpha__. Con el valor de alpha podemos darle transparencia a nuestro color. el valor va desde el 0 a 1.
```
p {
    background:rgba(0,0,0,1);
}
```

# hsla(hue, saturation%, lightness%, alpha)
La definicion hsla, es basado en 4 valores. El primer valor es matiz, el segundo la saturacion el tercero el brillo y el cuarto el valor alpha.
```
p {
    background-color:hsla(0, 100%, 50%, .8);
}
```


