---
title: Tipos de datos
---

Ahora que sabemos el propósito de las variables (almacenar datos y utilizarlos en nuestros procedimientos) pasemos a hablar de algunos tipos de datos que podemos guardar.


## Números

Si recordamos un poco de matemáticas básicas tenemos dos tipos de números: los enteros y los reales. La diferencia fundamental es que los números reales son los números enteros junto con los que tienen decimales. Un ejemplo de número entero es el 32 y un ejemplo de número real es el 43.5 (en Python se usa el punto en vez de la coma para separar la parte entera de la parte decimal.

Cuando en Python queremos trabajar con números enteros deberemos acordarnos de la palabra int y cuando necesitemos números reales recordaremos la palabra float.

### Convertir de un tipo a otro

Cuando le decimos el valor que tiene que tener una variable (esto se llama asignar) Python deduce automáticamente el tipo que queremos usar. En el siguiente ejemplo crearemos una variable que almacenará un número entero y otra que almacenará un número decimal.

```
entero=35
decimal=14.62
```

Si por alguna razón tenemos que convertir un float a int (para quedarnos con la parte entera) deberemos usar la función int recibe como parámetro aquello que necesitemos convertir a un número entero. El resultado de esta función lo asignaremos a una variable para que quede almacenado.

```
parteEntera=int(decimal)
```


## Cadenas de texto

Todo lo que escribamos en el teclado y todo lo que el ordenador tenga que imprimir en la pantalla se considera una cadena de texto. Se le llama cadena porque, como veremos más adelante, Python conoce el orden de cada uno de los caracteres que la componen. Si queremos almacenar un texto en una variable lo escribiremos entre comillas (como cuando lo imprimíamos con `print`).

```
principio="En un lugar de La Mancha"
```

Las cadenas se pueden convertir a números enteros con la función `int` o a números decimales con la función `float`. También podríamos convertir un número a una cadena con la función `str`.