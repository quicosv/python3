---
title: Comunicación con el usuario
---

Al crear nuestro primer programa hicimos que Python imprimiera varias cadenas en la pantalla. Ahora veremos un poco más sobre la función `print` y sobre cómo pedir datos al usuario.


## Más sobre `print`

Veamos cómo, además de las cadenas, también se puede mostrar por pantalla el contenido de las variables.

```
entero=15
decimal=27.3
mensaje="Esto es una prueba."
print(entero)
print(decimal)
print(mensaje)
print("mensaje")
```

En las tres primeras líneas se asignan los valores a las variables. La parte importante de este código es cuando las imprimimos. Debe quedar claro que si queremos imprimir un texto, éste debe ir siempre entre comillas. Sin embargo, los nombres de las variables no van entre comillas.


Combinar texto y variables

Para imprimir un texto en el que necesitamos que Python sustituya el contenido de alguna variable realizaremos un procedimiento conocido como formatear la cadena, siguiendo estos pasos:

1. Escribiremos la cadena entre comillas como venmos haciendo hasta ahora.
1. En el punto en el que necesitemos que aparezca el contenido de una variable escribiremos los signos de abrir llave y cerrar llave (`{}`).
1. Al finalizar la cadena escribiremos un punto.
1. Después del punto llamaremos a la función `format` y le pasaremos como parámetros las variables con las que se va a realizar la sustitución en el orden correcto.


Nada mejor que un ejemplo para aclarar este concepto:

```
nombre="José Luis"
edad=35
altura=1.85
peso=70
print("Hola. Me llamo {}, tengo {} años, mido {} metros y peso {} kilos.".format(nombre,edad,altura,peso))
```


## Entrada de datos

Para que el usuario pueda teclear un dato usaremos la función `input`, que recibe como parámetro el texto que se mostrará al usuario para que teclee algo. Lo que teclee el usuario será procesado como tipo texto. Por lo tanto, si queremos que nos proporcionen el título de un libro no tenemos más que guardarlo en una variable.

```
titulo=input("Título del libro: ")
```

¿Qué pasa si necesitamos que nos escriban un número? Aquí también usaremos la función `input`, pero como no nos interesa trabajar con un texto, la pondremos como argumento de la función `int` o `float`, según necesitemos un número entero o decimal. Veamos el siguiente ejemplo:

```
piezas=int(input("Número de piezas: "))
```

Queremos que nos digan una cantidad de piezas. Por lo tanto, sabemos que vamos a almacenar un número entero (no existe un cuarto de pieza). Por lo tanto, usaremos la función `int`. Lo que ponemos dentro de los paréntesis es la función `input` que recibe la cantidad de piezas.

Podemos ver el procedimiento de la siguiente forma: El usuario ve un mensaje que dice «Número de piezas: «. Entonces teclea un número y pulsa intro. La función `input` lo captura y entrega un texto. Ese texto lo recoge la función `int` y lo transforma en un número entero. Para que no se pierda, lo almacenamos en la variable `piezas`.