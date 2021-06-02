---
title: Condicionales
---

No todos los problemas se pueden resolver como el que hemos puesto de ejemplo. En muchas ocasiones necesitaremos tomar una decisión en función de las circunstancias que ocurran. Analicemos el siguiente problema:

Una persona gana un premio en un juego de azar. Realizar un programa que diga si esta persona tiene que pagar impuestos, sabiendo que si el premio es de 1500 o menos no tiene que pagar.

A priori no sabemos la cantidad que tecleará el usuario, pero tenemos que hacer que el programa le dé el mensaje correcto. Para ello, tendremos que decirle que compruebe si el premio es mayor que 1500. Si es así, habrá que decir que esa persona debe pagar impuestos. En cambio, si esa condición no se cumple el programa debe decir que la persona no pagará impuestos.


## Los bloques

En el problema que estamos analizando y en otros muchos que veremos, tenemos grupos de instrucciones que pueden ejecutarse o no. Siguiendo con nuestro ejemplo, si la persona debe pagar impuestos no se ejecutará la parte que contenga el mensaje en el que se dice que no pagará impuestos. Para diferenciar qué instrucciones se ejecutarán en cada caso usamos bloques.

Reconoceremos la línea en la que se inicia el bloque porque termina con el signo de dos puntos (:). A partir de aquí, las líneas que estén dentro del bloque tendrán un nivel más de indentación que la línea anterior. Este nivel de indentación se consigue añadiendo al principio de la línea un tabulador o cuatro espacios. Cuando encontremos una línea con el nivel de indentación anterior interpretaremos que ya no está dentro del bloque.

Los usuarios de lectores de pantalla están obligados a revisar carcter por caracter el principio de cada línea para comprobar el nivel de indentación que tiene y saber qué está dentro de cada bloque, a no ser que tengan alguna aplicación que les diga el nivel de indentación de la línea en la que está el cursor.

## Ejemplo de bloques

```
Fuera de los bloques
Empieza el bloque 1:
	Dentro del bloque 1
	Empieza el bloque 2:
		Bloque 2 dentro del bloque 1
	Fuera del bloque 2 pero dentro del bloque 1
Fuera de los bloques
```


## Los bloques `if` y `else`

Ahora que sabemos lo que son los bloques definamos la forma de construir condiciones en Python:

```
if(condición a comprobar):
	Bloque si se cumple la condición
else:
	bloque si no se cumple la condición
```

Por lo tanto, si planteamos la condición de que el premio sea mayor que 1500, en el bloque del `if` imprimiremos que hay que pagar impuestos y en el bloque del `else` imprimiremos que no hay que pagar impuestos.

Por lo tanto, así quedaría el código de neustro programa:

```
premio=float(input("Importe del premio: "))
if(premio>1500):
	print("Esta persona tiene que pagar impuestos.")
else:
	print("Esta persona no tiene que pagar impuestos.")
```

El bloque `else` no es obligatorio. Podríamos hacer un programa que sólo imprimiera un mensaje cuando hay que pagar impuestos:

```
premio=float(input("Importe del premio: "))
if(premio>1500):
	print("Esta persona tiene que pagar impuestos.")
```


## El operador ternario

Si tanto el bloque del `if` como el bloque del else ocupan una sola línea podemos usar el operador ternario, que se estructura así:

```
si se cumple if(condicion) else si no se cumple
```

```
premio=float(input("Importe del premio: "))
print("Tiene que pagar impuestos.") if(premio>1500) else print("No tiene que pagar imuestos.")
```